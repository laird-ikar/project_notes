Une librarie C qui contient:
- [[socket]]
- [[setsockopt]]
- [[getsockname]]

# Domain
Sous macOS, la librairie supporte:
- `PF_LOCAL`: Protocoles locaux (host)
- `PF_UNIX`: (deprecated) Protocols locaux 
- `PF_INET`: Protocoles internet v4 (IPv4)
- `PF_ROUTE`: Protocoles de routages interne
- `PF_KEY`: Gestion de clés [doc here](https://www.rfc-editor.org/rfc/rfc2367)
- `PF_INET6`: Protocoles internet v6 (IPv6)
- `PF_SYSTEM`: Domaine du système (0 idee de ce que c'est)
- `PF_NDRV`: Acces brut au network
# Types
## struct sockaddr
```C
struct sockaddr{
	sa_family_t   sa_family; //address family
    char          sa_data[]; //socket address (variable-length data)
};
```
## sa_family_t
unsigned integral type (2-4 bytes)
