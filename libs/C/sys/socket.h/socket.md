Librairy: [[socket.h|<sys/socket.h>]]
Prototype: 
```C
int socket(int domain, int type, int protocol);
```
# Description
`socket()` crée un endpoint de communication et renvoie le `fd` de ce endpoint.
Le `domain` précise le type de communications et le type de protocole, ses valeurs possibles sont définies dans [[socket.h#domain|<sys/socket.h>]]. 
Le `type` précise le type de communication:
- `SOCK_STREAM`: TCP
- `SOCK_DGRAM`: UDP
- `SOCK_RAW`: socket pur (bas niveau)
Le `protocol` définis le protocole qui sera utilisé par le socket. En général, pour un `domain` et un `type` donné il n'y en a qu'un. Voir [[Liste détaillée des Protocoles]].
Renvoie `-1` en cas d'erreur, le `fd` du socket sinon.