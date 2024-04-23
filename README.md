# vaultwarden-docker-compose

## Introduction

This repository provides a Docker Compose configuration for setting up a self-hosted password manager using [Vaultwarden](https://github.com/dani-garcia/vaultwarden), a compatible server for the Bitwarden password manager.

## Features

- **Self-hosted:** Host your password manager on your own server for increased privacy and control.
- **Admin Page:** Enable an admin page to view registered users, delete users, and invite new users.
- **HTTPS Support:** Secure your connection with HTTPS to prevent possible MITM attacks.

## Getting Started

1. Clone this repository to your server:

    ```bash
    https://github.com/vineethmn/vaultwarden-docker-compose.git
    ```

2. Navigate to the cloned directory:

    ```bash
    cd vaultwarden-docker-compose
    ```

3. Edit the `.env` file and `config.json` file to configure your parameters.

4. Generate an authentication token for the admin page. It's recommended to use a long, randomly generated string of characters. You can use the following command to generate a token:

    ```bash
    openssl rand -base64 48
    ```

    Keep this token secret as it will be used as the password to access the admin area of your server.

5. Bring the `vaultwarden` container up

    ```bash
    docker compose up -d
    ```
   
6. Follow the instructions in the [Vaultwarden Wiki](https://github.com/dani-garcia/vaultwarden/wiki) for additional configuration and usage details.

## Security Note

It's heavily recommended to activate HTTPS before enabling the admin page to avoid possible MITM attacks.

## Additional Resources

- [Vaultwarden GitHub Repository](https://github.com/dani-garcia/vaultwarden)
- [Vaultwarden Wiki](https://github.com/dani-garcia/vaultwarden/wiki)
- [Blog Post: Setting Up a Self-Hosted Password Manager](https://geekscircuit.com/password-manager/)

## License

This project is licensed under the [MIT License](LICENSE).
