# Concepts
## Servers
osef, on gere que le cas minimal de 1 serveur et pleins de clients.
## Clients
Un truc connecté a un serveur qui n'est pas un serveur
### nickname 
[[nickname]] unique
### Informations que les serveurs doivent avoir
#### Vrai nom / Addresse 
- IP de l'host
- username du client sur cet host
- server au quel il est connecté
## operators
C'est genre les admins
pas donner sudo a connard
### ils peuvent faire quoi ?
ca peut varier lol
kick/ban
## channels
[[channel]] 
# Setup
port 6667 pour le plain text
port 6697 pour le TLS

# Client-to-Server
Ils communiquent par des string de bytes separés par des `\n` ou `\r`.
Les messages peuvent etre envoyé n'importe quand des deux cotes. 
Peut generer 0 ou plus de reponses.

UTF-8.

Noms des entités (client, serveur, channels) sont casemap (pas sensibles a la case);
Seveur doivent preciser le casemaping utilisé dans `RPL_ISUPPORT` qui est envoyé quand ça se  connecte.