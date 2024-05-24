1. Création d'un secret pour stocker les informations de la base de données utilisée par nextcloud.

```shell
kubectl create secret generic nextcloud-db-secret \
  --from-literal=mysql-root-password=ABCDEF123456! \
  --from-literal=mysql-database=nextdb \
  --from-literal=mysql-user=nextuser \
  --from-literal=mysql-password=ABCDEF123456!
```


2. Création d'un certificat SSL et d'une clé privée.

```shell
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout private.key -out certif.crt
```

3. Création d'un secret pour stocker la clé et le certificat.

```shell
kubectl create secret tls mon-certificat-tls --cert=certif.crt --key=private.key
```


> Problèmes à résoudre :
> - La redirection http > https ne fonctionne pas.
> - Le certificat servi n'est pas le bon.

