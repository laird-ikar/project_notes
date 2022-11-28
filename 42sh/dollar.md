#ft
Infos sur le comportement des dollar `$` dans les différents shells pour [[42/projects/42sh/42sh]].

# Bash
## $(...)
Dans bash, la syntaxe `$(...)` est une [[42/projects/42sh/Substitution de commande|substitution de commande]].

e.g. ``sudo chown $(id -u) /dir`` sera interprété comme `sudo chown 1000 /dir` (en considérant que mon user ID est `1000`) car ``$(id -u)`` est remplacé par l'output de `id -u` (i.e. `1000`  dans ce cas).

Il est possible d'imbriquer les [[42/projects/42sh/Substitution de commande|substitutions]] sans conditions particulières. Notons d'ailleurs que la commande est executée sans traitement particulier (les caractères gardent donc les même propriétés qu'à l'accoutumée).