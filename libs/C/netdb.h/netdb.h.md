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
## struct addrinfo
```C
struct addrinfo {
    int _ai_flags_;
    int _ai_family_;
    int _ai_socktype_;
    int _ai_protocol_;
    size_t _ai_addrlen_;
    char * _ai_canonname_;
    struct sockaddr * _ai_addr_;
    struct addrinfo * _ai_next_;
};
```