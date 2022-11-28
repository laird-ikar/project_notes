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
- [[Fonctions de C++98]]
- [[socket]]
- [[setsockopt]]
- [[getsockname]]
- [[getprotobyname]]
- [[gethostbyname]]
- [[getaddinfo]]
- [[freeaddrinfo]]
- [[bind]]
- [[connect]]
- [[listen]]
- [[accept]]
- [[htons]]
- [[htonl]]
- [[ntohs]]
- [[ntohl]]
- [[inet_addr]]
- [[inet_ntoa]]
- [[send]]
- [[recv]]
- [[signal]]
- [[lseek]]
- [[fstat]]
- [[fcntl]]
- [[poll]] , [[select]], [[kqueue]], ou [[epoll]]
n.b.: pas de [[fork]] et exactement 1 [[poll]] (ou equivalent) 
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
	- [[nickname]]
	- [[username]]
	- rejoindre [[channel]]
	- PM
	- tout message envoyé à un [[channel]] doit être envoyer à tout les clients qui ont rejoint ce channel
	- avoir des [[operators]] et des utilisateurs basiques
	- commandes spécifiques aux [[operators]]
- utiliser des descripteurs de fichier en mode non bloquant
	- mais **uniquement** avec ces flags : `fcntl(fd, F_SETFL, O_NONBLOCK);` 
- traiter absolument tout les problemes potentiels
	- [[Tests#nc sujet|test]] 
# Bonus
- envoie de fichier
- bot