
Servers SHOULD gerer `\n` seul et MAY gerer `\r` comme si c'etait `\r\n`
Server and client SHOULD ignore empty Line

Server devrait etre gentil et gerer les longs messages:
- renvoyer une erreur numerique (`ERR_INPUTTOOLONG` 417)
- truncate sur le 510e byte pour ajoute `\r\n` ou sur le dernier UTF-8
- ignorer le message et close la connection (mais faut pas faire ca plz)

server et client SHOULD NOT utiliser plus d'un espace dans les SPACE dans les [[RFC 1459 (Internet Relay Chat Protocol)#Format des messages|messages]]. 