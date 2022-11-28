Fonction de [[stdarg.h]]

# Prototype
```C
type va_arg(va_list ap, type);
```

On lui passe `ap` initialisée par [[va_start]]. Elle renvoie le prochain argment de la [[stdarg.h#va_list|va_list]] interprété comme une variable de type `type`.
Si le `type` n'est pas compatible avec le type du prochain élèment de la liste, ou que la liste est finie : c'est la sauce.