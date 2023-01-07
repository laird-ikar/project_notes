([[ft_irc]])
Tant que la registration n'est pas complete, le serveur MUST n'accepter que certaines commandes.

1. [[CAP]] LS 302
	- begin procedure de register 
2. [[PASS]]
	- pas necessaire, mais il MUST être avant la suite
3. [[NICK]] et [[USER]]
	- utiliser pour definir le nickname, l'username et le "real name" 
	- si pas de [[CAP]] negociation -> fin de la registration
4. Capability Negotiation
5. [[SASL]]
6. CAP END
	- end procedure de register 

Si tout ce passe bien, le serveur MUST renvoyer, dans cet ordre:
1. [[RPL_WELCOME]] (001)
2. [[RPL_YOURHOST]] (002)
3. [[RPL_CREATED]] (003)
4. [[RPL_MYINFO]] (004)
5. at leat one [[RPL_ISUPPORT]] (005)
Puis il SHOULD répondre comme si il avait reçu [[LUSERS]] et retourner les numerics appropriées.
Si le client a des client mods automatiques quand il rejoint le network, le serveur SHOULD envoyer [[RPL_UMODEIS]] (221).
Puis il MUST répondre comme si le client avait envoyé [[MOTD]] command (message of the day).
e.g. renvoyer le message of the day numerics ou [[ERR_NOMOTD]] (422).

Le premier parametre de [[RPL_WELCOME]] est le nickname assigné par le reseau au client. Les prochains changements de nickname seront communiqués par le serveur avec un [[NICK]].