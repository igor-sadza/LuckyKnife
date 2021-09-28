# SSO - Keycloak + Apache Guacamole

Guacamole saml with keycloak idp.

## Table of Contents

1. [Keycloak Configuration](#keycloak)
2. [Apache Guacamole Configuration](#sogo)

## Keycloak


## Apache Guacamole

Log in to your keycloak machine. 

Go to guacamole conf directory.

```sh
    cd /etc/guacamole 
```

Copy metadata link from keycloak admin page.

<img src="https://github.com/igor-sadza/JakCo/blob/74ff3497900190811ee770bfe531c4c0db0b2cec/sso/keycloak_sogo/img/19_ip_metadata.png" align="center">

Download metadata.

```sh
     wget -O metadata.xml https://YOUR-KEYCLOAK-INSTANCE/auth/realms/keycloak_sogo/protocol/saml/descriptor
```

Edit guacamole configuration file.

```sh
     vi /etc/guacamole/guacamole.properties
```

```sh
saml-idp-metadata-url: file:///etc/guacamole/guacamole.xml
saml-entity-id: https://YOUR-GUACAMOLE-INSTANCE
saml-callback-url: https://YOUR-GUACAMOLE-INSTANCE
saml-debug: true
saml-strict: true
```

Restart your Guacamole & Tomcat instances.

```sh
     systemctl restart tomcat9.service && systemctl restart guacd
```

Tomcat9 logs

```sh
     cat /var/log/tomcat9/catalina.out
```

Go to your guacamole webpage and login using keycloak credentials.

<img src="https://github.com/igor-sadza/JakCo/blob/74ff3497900190811ee770bfe531c4c0db0b2cec/sso/keycloak_sogo/img/18_login.png" align="center">




