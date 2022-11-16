Librairy: [[socket.h|<sys/socket.h>]]
Prototype: 
```C
int getsockname(int socket, struct sockaddr *restrict address, 
				socklen_t *restrict address_len);
```
# Description
`getsockname()` renvoie l'addresse courante du `socket` spécifié.
`address_len` doit représenté la mémoire allouée à `address`. Au retour, elle contiendra la taille de l'addresse retournée (en byte).
`address` est de type [[socket.h#struct sockaddr|struct sockaddr]].
Elle renvoie `0` en cas de succès, `-1` en cas d'erreur.