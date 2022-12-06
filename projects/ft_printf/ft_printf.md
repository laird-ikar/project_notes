Parce que ft_putnbr() et ft_putstr(), c’est pas assez.
# Sujet 
![[ft_printf.subject.pdf]]
# Compilation
- `gcc`
- `-Wall -Wextra -Werror`
# Fonctions autorisées
- [[libft]]
- [[malloc]]
- [[free]]
- [[write]]
- [[va_start]]
- [[va_arg]]
- [[va_copy]]
- [[va_end]]
# Processus de pensée 
Vu que je veux faire les bonus, va falloir parser.
Heureusement, j'ai fait minishell, donc on va pouvoir trouver un peu d'inspiration.
La premiére etape est de decouper notre string en modules (en fonction des flags)

Puis on parse tout les flags dans le string qu'ils sont censé être.
C'est la partie dure, on va passer par une [[Structure t_flag]]

On recole tout.
On print et on return.
And voila.

Bon va falloir passer par un buffer (i.e. char* + size_t) pour pouvoir print les characteres speciaux...

Vraiment quel enfer le padding.

`[normal padding spaces][sign symbole][0 padding][mainstr][left padding space]``

## Implementation des floats (pour plus tard)

symbole de signe + partie entiere + symbole separation + partie decimale