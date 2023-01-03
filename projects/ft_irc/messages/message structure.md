```
<message>       ::= ['@' <tags> <SPACE>] [':' <source> <SPACE> ] <command> [params] <crlf>
<tags>          ::= <tag> [';' <tag>]*
<tag>           ::= <key> ['=' <escaped_value>]
<key>           ::= [ <client_prefix> ] [ <vendor> '/' ] <key_name>
<client_prefix> ::= '+'
<key_name>      ::= <non-empty sequence of ascii letters, digits, hyphens ('-')>
<escaped_value> ::= <sequence of zero or more utf8 characters except NUL, CR, LF, semicolon (`;`) and SPACE>
<vendor>        ::= <host>
<SPACE>         ::= [' ']+
```
Memoire allouée: 512 bytes + 4096 bytes pour les tags.

e.g.
- tags:
	- `@id=123AB;rose` => `{"id": "123AB", "rose":""}`
	- `@url=;netsplit=tur,ty` => ``{"url": "", "netsplit": "tur,ty"}`

La source c'etait appele le prefix avant, ca a cette tête là :
`servername / (nickname ["!" user] ["@" host])`
client MUST NOT include source
server MAY include source

Les [[tags]] représentent un set de variables
La [[source]] représente l'origine du message
La [[command]] c'est la partie interressante du message. 