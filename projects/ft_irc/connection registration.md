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