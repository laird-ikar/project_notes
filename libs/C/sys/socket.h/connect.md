Librairy: [[socket.h|<sys/socket.h>]], [[types.h|<sys/types.h>]]
Prototype: 
```C
int connect(
	int socket,
	const struct sockaddr *address, 
	socklen_t *restrict address_len
	);
```
# Description
Si `socket` est de type `SOCK_DGRAM` `connect` associe le `socket` à `address`. Les datagrams sont envoyés dessus et c'est la seule addresse de la