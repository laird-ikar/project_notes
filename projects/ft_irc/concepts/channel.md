L'élément de base pour communiquer sur un IRC.
Il est définis par la liste des utilisateurs qui y sont connectés.
Pour le rejoindre (ou le créer s'il n'existe pas) l'utilisateur utilise la commande `join`.

Tout les clients connectés recoivent messages envoyé dessus.

Créé quand la premiere personne le rejoint.
Detruit quand la derniere se barre.
Referencable par son nom tant qu'il existe.

# Noms de channels
String
- MUST commencer par [[#type prefixes]]
- MUST NOT contenir ` \x07,`
## channels types
- regular: 
	- connu de tout les serveurs
	- `#`
- local:
	- serveur spécifique (tu peux que voir/parler aux gens connectés au meme serveur)
	- `&`

# Créer / Rejoindre
Commande : `JOIN`
Si le channel n'existe pas :
- Il est créé
- Le createur devient l'operator
Si le channel existe deja:
- Le gens se join selon les [[#requirements]] 
	- e.g. invite-only mode (`+i`) le client peut se joindre iff il a été invité par un autre user ou si il a été exempté par le [[operators]].
Tu peux en joindre autant que tu veux (sauf si limite imposée par serveur `CHANLIMIT`).
# Topic
Description du channel ; tout le monde le voit en se connectant. Et tout le monde est notifié quand ça change.
# Requirements
## invite only
`+i`
## topic
`+t`