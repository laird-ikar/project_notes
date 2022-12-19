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
- `POLLERR`: An exceptional condition has occurred on the device or socket.  This flag is output only, and ignored if present in the input events bitmask.
- 