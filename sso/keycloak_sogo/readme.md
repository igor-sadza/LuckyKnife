# SSO - Keycloak + SOGo

I prepare this HOW-TO for everyone who wants to use saml with SOGo.

## Table of Contents

1. [Keycloak configuration](#keycloak)
2. [SOGo configuration](#sogo)

## Keycloak

Login to your keycloak admin console and go to clients panel.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/0_clients.png" align="center"
     alt="Size Limit logo by Anton Lovchikov" >

Press create.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/1_create_client.png" align="center">

Open network browser, go to your sogo metadata page and save it.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/4_metadata.png" align="center">

Back to keycloak and press select file.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/2_import.png" align="center">

Select your save sogo xml config, press open.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/5_select.png" align="center">

Save your imported client.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/6_save.png" align="center">

Go to client mappers tab.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/7_mappers.png" align="center">

Hit create.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/8_create_mapper.png" align="center">

Create mail mapper

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/9_email_mapper.png" align="center">

Create username mapper

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/10_username_mapper.png" align="center">

Select users tab.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/11_users.png" align="center">

Press add user

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/12_add_user.png" align="center">

Save newly created user.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/13_save_created_user.png" align="center">

Go to user attributes.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/14_user_attributes.png" align="center">

Create mail attribute.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/15_save_attributes.png" align="center">

Go to user credentials.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/16_user_credentials.png" align="center">

Set user password.

<img src="https://github.com/igor-sadza/JakCo/blob/5147a7b527df4d6af8e3f277072e4e6d7fc91f44/sso/keycloak_sogo/img/17_set_password.png" align="center">

## SOGo
