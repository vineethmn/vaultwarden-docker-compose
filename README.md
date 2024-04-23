vaultwarden-docker-compose
Introduction
This repository provides a Docker Compose configuration for setting up a self-hosted password manager using Vaultwarden, a compatible server for the Bitwarden password manager.

Features
Self-hosted: Host your password manager on your own server for increased privacy and control.
Admin Page: Enable an admin page to view registered users, delete users, and invite new users.
HTTPS Support: Secure your connection with HTTPS to prevent possible MITM attacks.
Getting Started
Clone this repository to your server:
bash
Copy code
git clone https://github.com/vineethmn/vaultwarden-docker-compose.git
Navigate to the cloned directory:
bash
Copy code
cd vaultwarden-docker-compose
Edit the .env file and config.json file to configure your parameters.
Generate an authentication token for the admin page. It's recommended to use a long, randomly generated string of characters. You can use the following command to generate a token:
bash
Copy code
openssl rand -base64 48
Keep this token secret as it will be used as the password to access the admin area of your server.
Follow the instructions in the Vaultwarden Wiki for additional configuration and usage details.
Security Note
It's heavily recommended to activate HTTPS before enabling the admin page to avoid possible MITM attacks.

Additional Resources
Vaultwarden GitHub Repository
Vaultwarden Wiki
Blog Post: Setting Up a Self-Hosted Password Manager
License
This project is licensed under the MIT License.
