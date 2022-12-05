# One-to-one
C'est des mp, y'a que les clients impliqué et les serveurs par qui ça passe qui voient.
C'est straight forward :)
# One-to-many
## To channel
Ça envoie à tout les les clients connectés à un channel sauf l'envoyeur.
- si 1 connard: le serveur garde pour lui
- si 2: mp
- si +: broadcast -1 
## To host/server mask
C'est comme les [[channel]] mais par IP + mask.
## To list
Tu fais une liste de user et le serveur envoie une copie a toute les personnes de la liste ?
C'est tout cassé faut pas faire ça.
# One-to-all
broadcast: t'envoie a tout le monde