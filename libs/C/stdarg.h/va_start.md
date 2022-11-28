Fonction de [[stdarg.h]]

# Prototype
```C
type va_start(va_list ap, last);
```
# Description
Doit être appelée en premier. Elle initialise la [[stdarg.h#va_list|va_list]] pour la rendre utilisable.
Necessite d'appeler [[va_end]] dans la même fonction (pour liberer la [[stdarg.h#va_list|va_list]]).