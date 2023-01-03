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

e.g.
	- `@id=123AB;rose` => `{"id": "123AB", "rose":""}`
	- `@url=;netsplit=tur,ty` => ``{"url": "", "netsplit": "tur,ty"}`

Une clé peut être utilisée au plus 1 fois par message, mais si jamais on reçoit plus d'une fois une clé on SHOULD prendre en compte la derniere.

# Escaping values
| Character     | Sequence in `<escaped_value>`      |
| ----------    | ------------------------------ |
| ; (semicolon) | `\:`                             |
| SPACE         | `\s`                             |
| `\`             | `\\`                             |
| CR           | `\r`                              |
| LF           | `\n`                              |
| all others   | the character itself            |

Si jamais il y a un `\` seul à la fin de l'escaped ou si il y a un `\` suivi d'un charactere non valide, on SHOULD ignorer.
e.g.
- 