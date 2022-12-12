Librairy: [[socket.h|<sys/socket.h>]], [[types.h|<sys/types.h>]], [[netdb.h|<netdb.h>]]
Prototype: 
```C
int getaddrinfo(
	const char *hostname,
	const char *servname,
	const struct addrinfo *hints,
	struct addrinfo **res
	);
```
# Description
La fonction est utilisée pour récupérer une liste d'IP et de ports pour `hostname` et `servname`. C'est un remplaçant plus flexible à [[gethostbyname]] et [[getservbyname]].

`hostname` et `servname` sont soit un `char *` nul-terminé ou `NULL`.
`hostname` accepte soit un nom d'hôte valide ou une addresse IP (v4 ou v6).
`servname` accepte soit un numéro de port ou un nom de service (listé par [[services]]).
Au moins un des deux doit être non-null.

`hints` est un pointeur optionel vers une structure [[netdb.h#struct addrinfo|addrinfo]].
Elle sert à donner des indices sur le type de socket 