Librairy: [[socket.h|<sys/socket.h>]]
Prototype: 
```C
int bind(
	int socket,
	const struct sockaddr *address,
    socklen_t address_len
    );
```
# Description
`bind` assigne un nom à un socket sans nom.
Quans un socket est créé avec [[socket]], il existe dans un namespace (la famille d'addresse) mais n'a pas de nom.
`bind` fait une requete pour associer `address` au `socket`. Si la requete aboutie, il retourne 0, -1 sinon.