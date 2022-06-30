
<details>
<summary markdown="span">Windows LCST</summary>
<h1 align="center" id="heading"><a href="https://isofiles.bd581e55.workers.dev/Windows%2010/Windows%2010%20Enterprise%20LTSC%202021/"> Windows LCST </a></h1>  
  
 
"A version of windows 10 that is completely free of bloatware (no Microsoft store, no preinstalled apps like candy crush, no tiles on start menu, no Cortana, only windows search, no edge, only Internet explorer). It only gets security updates instead of feature updates, and has support for 10 years. Best version of windows 10 IMO. FYI it was originally called LTSB (Long term servicing branch) and was renamed to LTSC (Long term servicing channel). "

:exclamation: [Create Windows 10 ISO image from Existing Installation](https://www.tenforums.com/tutorials/72031-create-windows-10-iso-image-existing-installation.html#Part4)
____________________________________________________________________________________________ 
</details>

<details>
<summary markdown="span">Chocolatealy</summary>
<h1 align="center" id="heading"><a href="https://chocolatey.org/why-chocolatey"> Chocolatealy </a></h1>  

Chocolatey is software management automation for Windows that wraps installers, executables, zips, and scripts into compiled packages.

###### PowerShell script: 
```yaml
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1')); choco install chocolateygui
```
____________________________________________________________________________________________ 
</details>

<details>
<summary markdown="span">Unlock Builtin Administrator</summary>
<h1 align="center" id="heading"> Unlock Builtin Administrator </h1>
  
With great power, comes great responsibility!
  
###### PowerShell script: 
```yaml
Start-Process powershell -verb RunAs -ArgumentList 'Get-LocalUser -Name "Administrator" | Enable-LocalUser'
```
____________________________________________________________________________________________ 
</details>

<details>
<summary markdown="span">Passwordless RDP</summary>
<h1 align="center" id="heading"> Passwordless RDP </h1>
  
###### PowerShell script: 
```yaml
Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "UserAuthentication" -Value 0;
Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Terminal Server'-name "fDenyTSConnections" -Value 0;
Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Lsa'-name "LimitBlankPasswordUse" -Value 0;
Enable-NetFirewallRule -DisplayGroup "Remote Desktop";
```
____________________________________________________________________________________________ 
</details>

<details>
<summary markdown="span">Edge Remover</summary>
<h1 align="center" id="heading"><a href="https://gist.github.com/ishad0w/d25ca52eb04dbefba8087a344a69c79c">Edge Remover</a></h1>
  
###### PowerShell script: 
```yaml
$sPath=[Environment]::GetFolderPath("Desktop")+"\script.bat";curl https://gist.githubusercontent.com/ishad0w/d25ca52eb04dbefba8087a344a69c79c/raw/27e1e32a40c82f5dc46a81dca87ba8842616ae03/microsoft_edge_uninstaller_21h1_ltsc.bat -o $sPath; Start-Process powershell -verb RunAs -ArgumentList "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; $sPath" -Wait; Remove-Item $sPath
```
____________________________________________________________________________________________ 
</details>

<details>
<summary markdown="span">Windows Debloater</summary>
<h1 align="center" id="heading"><a href="https://github.com/Sycnex/Windows10Debloater">Windows Debloater</a></h1>
  
Script/Utility/Application to debloat Windows 10, to remove Windows pre-installed unnecessary applications, stop some telemetry functions, stop Cortana from being used as your Search Index, disable unnecessary scheduled tasks, and more...

###### PowerShell script: 
```yaml
$sPath=[Environment]::GetFolderPath("Desktop")+"\script.ps1";curl https://raw.githubusercontent.com/Sycnex/Windows10Debloater/master/Windows10DebloaterGUI.ps1 -o $sPath; Start-Process powershell -verb RunAs -ArgumentList "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; $sPath" -Wait; Remove-Item $sPath
```
____________________________________________________________________________________________ 
</details>

<details>
<summary markdown="span">MAS - Activator</summary>
<h1 align="center" id="heading"><a href="https://github.com/massgravel/Microsoft-Activation-Scripts">MAS</a></h1>
  
A collection of scripts for activating Microsoft products using HWID / KMS38 / Online KMS activation methods with a focus on open-source code, less antivirus detection and user-friendliness.

###### PowerShell script: 
```yaml
$sPath=[Environment]::GetFolderPath("Desktop")+"\script.cmd";curl https://raw.githubusercontent.com/massgravel/Microsoft-Activation-Scripts/master/MAS/All-In-One-Version/MAS_1.5_AIO_CRC32_21D20776.cmd -o $sPath; Start-Process powershell -verb RunAs -ArgumentList "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; $sPath" -Wait; Remove-Item $sPath
```
____________________________________________________________________________________________ 
</details>
