<!-- ABOUT THE PROJECT -->
## Bitwarden Mail Settings

Mail settings for your bitwarden self hosted service.

### Installation

Put this global settings in your bitwarden override file.

1. Edit global.override.env
```sh
vi ~/bwdata/env/global.override.env
```
2. Put parameters
```sh
globalSettings__mail__replyToEmail=no-reply@YOUR-DOMAIN
globalSettings__mail__smtp__host=YOUR-DOMAIN
globalSettings__mail__smtp__username=VALID-USERNAME
globalSettings__mail__smtp__password=VALID-PASSWORD
globalSettings__mail__smtp__ssl=false
globalSettings__mail__smtp__port=587
globalSettings__mail__smtp__useDefaultCredentials=false
globalSettings__mail__smtp__authType=Negotiate
globalSettings__mail__smtp__trustServer=true
```


