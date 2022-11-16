# Réseau
Un réseau c'est tout plein de machines qui partagent un masque et une ip réseau.
La taille d'un réseau est définis par le nombre de 0 de son masque : si un masque contient `n` 0s, il permet `2 ^ n` IPs.
.e.g
- un réseau avec le masque 255.255.255.252 (/30) ne possède que 4 IPs
- un réseau avec le masque 255.255.255.192 (/26) possède 64 ips.
## Masque /X
À partir d'un masque sous forme /X, on peut faire `2 ^ (32 - X)` pour connaître le nombre d'IPs.
## Masque A.B.C.D
À partir d'un masque sous forme A.B.C.D on _apprend_ les 8 correspondances suivantes : 
8. 0
7. 128
6. 192
5. 224
4. 240
3. 248
2. 252
1. 254
0. 255
Le nombre d'ip est la somme des indices 
e.g. 255.255.240.0 : `8 + 8 + 4 + 0 = 2 ^ 20` machines.
## Arnaque Moldave
Si le masque est inférieur à /24 (i.e. X.Y.Z.0) on peut juste rester dans des IPs qui partages toutes les 3 premiers chiffres en n'en avoir rien a fouttre. 
Sinon on prend des IP voisines (i.e. 133.8.4.1 et 133.8.4.2) en faisant attention à ne pas prendre une IP réseau ou broadcast (en gros on evite les `2 ^ n` et les `2 ^ n -1`).