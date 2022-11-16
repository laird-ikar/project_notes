Librairy: [[netdb.h|<netdb.h>]]
Prototype: 
```C
struct protoent *getprotobyname(const char *name);
```
# Description
Parcours [[Liste détaillée des Protocoles]] jusqu'au premier protocole dont le nom correspond à `name` ou un `EOF` en renvoie un pointeur vers un [[netdb.h#struct protoent|struct prototen]] correspondant au protocole (ou NULL en cas d'erreur).