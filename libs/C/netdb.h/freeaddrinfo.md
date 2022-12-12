Librairy: [[socket.h|<sys/socket.h>]], [[types.h|<sys/types.h>]], [[netdb.h|<netdb.h>]]
Prototype: 
```C
void freeaddrinfo(struct addrinfo *ai);
```
# Description
Libère la [[netdb.h#struct addrinfo|addrinfo]] allouée par un [[getaddrinfo]] réussis.