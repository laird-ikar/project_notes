Librairy: [[socket.h|<sys/socket.h>]]
Prototype:
```C
int setsockopt(int socket, int level, int option_name, const void *option_value, 
			   socklen_t option_len);
```
# Description
`setsockopt()` manipule les options associées à un `socket`.
Il faut préciser le `level` de l'option que l'on veut éditer. 
- `SOC_SOCKET`: Manipuler les options du `socket`
- Pour manipuler les options au niveau du protocole, il faut entrer le protocol number
	- e.g.: Si on veut toucher une option de TCP, il faut récupérer son protocol number (voir [[getprotobyname]])
Les paramètres `option_value` et `option_len` sont utilisées pour acceder aux valeurs des options.
Renvoie `0` si tout va bien, `-1` sinon.
## Options au niveau socket
- `SO_DEBUG`: `int`, active l'enregistrement des infomations de debug
- `SO_REUSEADDR`: `int`, active la réutilisation d'addresse locale
- `SO_REUSEPORT`: `int`, active les doublons d'addresse:port
- `SO_KEEPALIVE`: `int`, active la connection persistente
- `SO_DONTROUTE`: `int`, active le bypass des routes pour les messages sortants
- `SO_LINGER`: `int`, modifie le comportement de `close()` (utilisation rare)
- `SO_LINGER_SEC`: `int`, time out de linger
- `SO_BROADCAST`: `int`, active la transmission en broadcast
- `SO_OOBINLINE`: `int`, active la reception de data out-of-band
- `SO_SNDBUF`: `int`, taille du buffer d'output
- `SO_RCVBUF`: `int`, taille du buffer d'input
- `SO_SNDLOWAT`: `int`, taille minimum (en byte) d'un output
- `SO_RCVLOWAT`: `int`, taille minimum (en byte) d'un input
- `SO_SNDTIMEO`: `struct timeval`, time-out en output
- `SO_RCVTIMEO`: `struct timeval`, time-out en input
- `SO_NOSIGPIPE`: `int`, renvoie des `EPIPE`s au lieu de générer des `SIGPIPE`s