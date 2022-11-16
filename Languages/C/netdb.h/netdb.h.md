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
