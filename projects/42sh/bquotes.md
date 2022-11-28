#ft
Infos sur le comportement des backquotes \` dans les différents shells pour [[42/holygraph/projects/42sh/42sh]].

# Bash

Dans bash, la syntaxe`` `...` ``est une [[42/holygraph/projects/42sh/Substitution de commande|substitution de commande]]. C'est par contre la notation ancienne de cette fonctionnalité.

e.g. ``sudo chown `id -u` /dir`` sera interprété comme `sudo chown 1000 /dir` (en considérant que mon user ID est `1000`) car`` `id -u` ``est remplacé par l'output de `id -u` (i.e. `1000`  dans ce cas).

La substitution s'arrete au premier \` qui n'est pas précédé d'un \\. 
Ici le \\ a une valeur littérale sauf s'il précède un \\, un $, ou un \`. 
Il est possible d'imbriquer les [[42/holygraph/projects/42sh/Substitution de commande|substitutions]] en escapant les \` dans la commande substituée.