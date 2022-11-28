Fonction de la librairie [[unistd.h]]
# Prototype
```C
ssize_t write(int fildes, const void *buf, size_t nbyte);
```
# Description
Essaye d'écrire `nbytes` de data depuis `buf` vers l'objet décris par `fildes`.
Renvoie le nombre de bytes écrits, ou `-1` en cas d'échec.