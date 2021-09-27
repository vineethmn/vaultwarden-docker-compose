# vaultwarden-docker-compose
A self hosted password manager, 


Enabling admin page

IMPORTANT: It's heavily recommended to activate HTTPS before enabling this feature, to avoid possible MITM attacks.

This page allows a server administrator to view all the registered users and to delete them. It also allows inviting new users, even when registration is disabled.

To enable the admin page, you need to set an authentication token. This token can be anything, but it's recommended to use a long, randomly generated string of characters, for example running openssl rand -base64 48. Keep this token secret, this is the password to access the admin area of your server!

Note : edit .env file with your parameters


All documents can be found here : @https://github.com/dani-garcia/vaultwarden/wiki
