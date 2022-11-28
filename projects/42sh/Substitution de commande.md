#ft
Selon le manuel de bash, entrée [3.5.4 Command Subsitution](https://www.gnu.org/software/bash/manual/html_node/Command-Substitution.html), une commande de substitution permet d'inserer l'output d'une commande à l’intérieur d'une autre commande.

Il y a pour ça deux syntaxes : `$(...)` et `` `...` ``.
Les deux syntaxes ne sont pas exactement identiques (voir [[dollar#$(...)|dollar]] ou [[bquotes#Bash|bquotes]]).

Dans les deux cas, bash performe `...` dans un subshell et remplace le token d'execution par la sortie standard dont les retours à la ligne finaux ont été supprimés (i.e. `returned\nValue\n\n`  => `returned\nvalue`).