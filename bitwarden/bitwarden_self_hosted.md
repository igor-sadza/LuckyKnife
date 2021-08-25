
apt-get install curl sudo git

sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian \
$(lsb_release -cs) \
stable"

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb

sudo dpkg -i packages-microsoft-prod.deb

sudo apt-get install -y apt-transport-https && sudo apt-get update && sudo apt-get install -y dotnet-sdk-5.0

git clone https://github.com/jakeswenson/BitBetter.git

cd BitBetter
./build.sh

vi ~/bwdata/docker/docker-compose.override.yml
---
version: '3'

services:
  api:
    image: bitbetter/api

  identity:
    image: bitbetter/identity
---

vi ~/bwdata/scripts/run.sh
---
Replace dockerComposePull
with #dockerComposePull
---

./build.sh
./run.sh interactive

cd
ls
./*.sh
./*.sh restart
./*.sh stop

cd BitBetter
ls
./build.sh
ls
./upd*
sudo shutdown
sudo shutdown now


https://bitwarden.com/help/article/install-on-premise/
https://docs.microsoft.com/en-us/dotnet/core/install/linux-debian
https://github.com/jakeswenson/BitBetter
