Ce dossier contient les fichiers de configuration nécessaires pour déployer un serveur VPN WireGuard avec une interface graphique WireGuard, le tout orchestré avec Docker Compose. Cette solution offre une méthode simple et efficace pour mettre en place un réseau privé virtuel sécurisé.

## Prérequis

Avant de commencer, assurez-vous d'avoir installé Docker et Docker Compose sur votre système. Vous pouvez trouver des instructions d'installation sur le site officiel de Docker :

- Docker
- Docker Compose

## Installation

1. Copiez les fichiers `default.conf`et `docker-compose.yml`dans le réperoire de votre projet.
2. Créez le répertoire `ssl_certs` à la racine de votre projet.
3. Déposez votre clé privée et votre certificat SSL dans le répertoire `ssl_certs`.
4. Modifiez le fichier `default.conf` en remplaçant les directives `server_name` pour qu'elles correspondent à votre nom de domaine.
5. Utilisez la commande `docker-compose up -d` pour déployer votre stack WireGuard.

