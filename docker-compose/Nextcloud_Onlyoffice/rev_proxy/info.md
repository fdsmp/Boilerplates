
Créez le répertoire `certs` dans répertoire ou se trouve le fichier docker-compose.yml. 
Déposez le certificat, la clé et le cachain dans le répertoire certs.

Placez les fichiers `httpd.conf` et `httpd-ssl.conf` dans le répertoire racine du projet.
    -> Remplacez `nextcloud_dns_name` et `onlyoffice_dns_name` par les noms de domaines de vos serveur nextcloud et onlyoffice.


Configuration de nextcloud :

Editez le fichier `config.php`(html/config.config.ph)

1. Ajoutez les domaines approvés :

Exemple: nextcloud.test.local et onlyoffice.test.local

```php
  'trusted_domains' => 
  array (
    0 => 'nextcloud.test.local',
    1 => 'onlyoffice.test.local',
  ),
```

2. Ajoutez la liste des serveurs proxies approuvés:

```php
'trusted_proxies' => array ( 0 => 'http://your_proxy_ip', ),
```

