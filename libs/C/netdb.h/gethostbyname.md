Librairy: [[netdb.h|<netdb.h>]]
Prototype: 
```C
struct hostent *gethostbyname(const char *name);
```
# Description
Renvoie une structure de type [[netdb.h#struct hostent|hostent]] pour l'hôte `name`. 
`name` est soit un nom d'hôte, soit une IPv4, soit une IPv6 ([source](http://manpagesfr.free.fr/man/man3/gethostbyname.3.html)). Si c'est une IP il n'y a pas de recherche et `name` est copié dans `h_name` et son equivalent [[in_addr]] dans `h_addr_list[0]` de la struture retournée.