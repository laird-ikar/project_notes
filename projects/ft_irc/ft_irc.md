Projet [[42]] pour faire joujou avec les serveurs.
C'est un projet de groupe. Je le fais avec:
- [[Bruno Dehais]]
# Résumé  
L’objectif de ce projet est de reproduire le fonctionnement d’un serveur IRC.  
Vous utiliserez un vrai client IRC afin de vous connecter à votre serveur et ainsi de le  
tester.  
Internet fonctionne grâce à de nombreux standards et protocoles pour permettre une  
interopérabilité entre les machines connectées. Il est toujours intéressant de connaître ce  
genre de chose.

# Sujet
![[ft_irc.fr.subject.pdf]]
# Compilation
- `c++`
- `-Wall -Wextra -Werror` (obligatoire)
- `-std=c++98` (doit compiler avec)
# Fonctions autorisées
- [[42/holygraph/libs/to_class/Fonctions de C++98]]
- [[socket]]
- [[setsockopt]]
- [[getsockname]]
- [[getprotobyname]]
- [[gethostbyname]]
- [[42/holygraph/libs/to_class/getaddinfo]]
- [[42/holygraph/libs/to_class/freeaddrinfo]]
- [[42/holygraph/libs/to_class/bind]]
- [[42/holygraph/libs/to_class/connect]]
- [[42/holygraph/libs/to_class/listen]]
- [[42/holygraph/libs/to_class/accept]]
- [[42/holygraph/libs/to_class/htons]]
- [[42/holygraph/libs/to_class/htonl]]
- [[42/holygraph/libs/to_class/ntohs]]
- [[42/holygraph/libs/to_class/ntohl]]
- [[42/holygraph/libs/to_class/inet_addr]]
- [[42/holygraph/libs/to_class/inet_ntoa]]
- [[42/holygraph/libs/to_class/send]]
- [[42/holygraph/libs/to_class/recv]]
- [[42/holygraph/libs/to_class/signal]]
- [[42/holygraph/libs/to_class/lseek]]
- [[42/holygraph/libs/to_class/fstat]]
- [[42/holygraph/libs/to_class/fcntl]]
- [[42/holygraph/libs/to_class/poll]] , [[42/holygraph/libs/to_class/select]], [[42/holygraph/libs/to_class/kqueue]], ou [[42/holygraph/libs/to_class/epoll]]
n.b.: pas de [[42/holygraph/libs/to_class/fork]] et exactement 1 [[42/holygraph/libs/to_class/poll]] (ou equivalent) 
# Execution
`./ircserv <port> <password>` 
- `<port>`: numéro du port sur lequel on accepte les connexions
- `<password>`: mot de passe permettant de s'identifier (clients doivent le fournir)


# Prérequis
- Possibilité d'avoir plusieurs clients en même temps.
- Communication client/server en TCP/IP (v4 ou v6)
- Ne dois jamais bloquer
- Définir un client IRC comme référence (il sera utiliser en évaluation)
- Utilisation avec notre serveur ≈ utilisation avec un vrai serveur. Fonctionnalitées obligatoires :
	- S'authentifier
	- [[42/holygraph/projects/ft_irc/nickname]]
	- [[42/holygraph/projects/ft_irc/username]]
	- rejoindre [[42/holygraph/projects/ft_irc/channel]]
	- PM
	- tout message envoyé à un [[42/holygraph/projects/ft_irc/channel]] doit être envoyer à tout les clients qui ont rejoint ce channel
	- avoir des [[42/holygraph/projects/ft_irc/operators]] et des utilisateurs basiques
	- commandes spécifiques aux [[42/holygraph/projects/ft_irc/operators]]
- utiliser des descripteurs de fichier en mode non bloquant
	- mais **uniquement** avec ces flags : `fcntl(fd, F_SETFL, O_NONBLOCK);` 
- traiter absolument tout les problemes potentiels
	- [[42/holygraph/projects/ft_irc/Tests#nc sujet|test]] 
# Bonus
- envoie de fichier
- bot