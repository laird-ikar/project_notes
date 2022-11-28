Une librarie C qui contient:
- [[getprotobyname]]
- [[gethostbyname]]
# Types
## struct protoent
```C
struct  protoent {
	   char    *p_name;        /* official name of protocol */
	   char    **p_aliases;    /* alias list */
	   int     p_proto;        /* protocol number */
};
```
## struct hostent
```C
struct hostent {
	char  *h_name;            /* official name of host */
	char **h_aliases;         /* alias list */
	int    h_addrtype;        /* host address type */
	int    h_length;          /* length of address */
	char **h_addr_list;       /* list of addresses */
};
```
