# Fonctions
- [[poll]]

# Structure
## pollfd
```C
     struct pollfd {
         int    fd;       /* file descriptor */
         short  events;   /* events to look for */
         short  revents;  /* events returned */
     };
```

# Macros
## Flags
- `POLLERR`: 