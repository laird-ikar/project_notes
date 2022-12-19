Librairy: [[poll.h|<poll.h>]]
# Prototype: 
```C
int poll(struct pollfd fds[], nfds_t nfds, int timeout);
```
# Description
Check tout les fd de la [[poll.h#pollfd|pollfd]] en fonctions des [[poll.h#flags|flags]] inscrit dedans et retourne le nombre le nombre de fd pret pour I/O.
`nfds` est la taille de `fds`.
`timeout` est le temps maximum que `poll()` passe à inte