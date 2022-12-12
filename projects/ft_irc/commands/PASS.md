```
command: PASS
parameters: <password>
```
Si il est envoyé il doit être set avant [[NICK]] et [[USER]].
`<password>` MUST correspondre avec celui defini dans la config du server.
Si t'en envoies plusieurs, on prend en compte que le dernier.
Si ca match pas, le serveur SHOULD envoyer [[ERR_PASSWDMISMATCH]] (464) et MAY fermer la connection avec [[ERROR]]. (MUST send a least one these two).

Numeric replies:

-   [[ERR_NEEDMOREPARAMS]] (461)
-   [[ERR_ALREADYREGISTERED]] (462)
-   [[ERR_PASSWDMISMATCH]] (464)
