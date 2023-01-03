```
<tags>          ::= <tag> [';' <tag>]*
<tag>           ::= <key> ['=' <escaped_value>]
<key>           ::= [ <client_prefix> ] [ <vendor> '/' ] <key_name>
<client_prefix> ::= '+'
<key_name>      ::= <non-empty sequence of ascii letters, digits, hyphens ('-')>
<escaped_value> ::= <sequence of zero or more utf8 characters except NUL, CR, LF, semicolon (`;`) and SPACE>
<vendor>        ::= <host>
```

Si le message contient des tags, ils seront interprétés comme une suite de keys et values.
Une clé peut être utilisée au plus 1 fois par message, mais si jamais on reçoit plus d'un 


e.g.
	- `@id=123AB;rose` => `{"id": "123AB", "rose":""}`
	- `@url=;netsplit=tur,ty` => ``{"url": "", "netsplit": "tur,ty"}`