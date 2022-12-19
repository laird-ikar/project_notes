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
  An exceptional condition has occurred on the device or socket.  This flag is output only, and ignored if present in the input events bitmask.
- POLLHUP:
  The device or socket has been disconnected.  This flag is output only, and ignored if present in the input events bitmask.  Note that POLLHUP and POLLOUT are mutually exclusive and should never be present in the revents bit-mask at the same time.
- POLLIN:
  Data other than high priority data may be read without blocking.  This is equivalent to POLLRDNORM | POLLRDBAND).

     POLLNVAL       The file descriptor is not open.  This flag is output
                    only, and ignored if present in the input events bitmask.

     POLLOUT        Normal data may be written without blocking.  This is
                    equivalent to POLLWRNORM.

     POLLPRI        High priority data may be read without blocking.

     POLLRDBAND     Priority data may be read without blocking.

     POLLRDNORM     Normal data may be read without blocking.

     POLLWRBAND     Priority data may be written without blocking.

     POLLWRNORM     Normal data may be written without blocking.