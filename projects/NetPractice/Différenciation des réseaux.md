# Différenciation des réseaux
Afin de pouvoir faire communiquer entre elles deux machines A et B qui ne sont pas directement connectées, leurs IP doivent faire partie de plage d'addresse différentes.

C'est à dire que `ipA & maskA ≠ ipB & maskB`

i.e.
Si A a l'addresse 45.187.30.6/26 et qu'elle veut communiquer avec une machine B qui ne fait pas parti de son réseau local, il faut **impérativement** que B ne soit **pas** entre 45.187.30.0 et 45.187.30.63.

## Concrètement pour l'exo 8
![[net practice 8.png]]
Internet veut aller pecho du 

X.Y.Z.0/26

Du coup

D1 et C1 doivent être entre 
X.Y.Z.0 et X.Y.Z.63
Et vu que D1 est forcé d'avoir un masque 255.255.255.240 (aka /28) toute la plage entre X.Y.Z.0 et  X.Y.Z.15 (en supposant qu'on met un D dans cette plage) est reservé pour son reseau local.

du coup en solution facile qui marche a tout les coups
- D1: X.Y.Z.1/28
	- R23: X.Y.Z.2/28
- C1: X.Y.Z.61/30
	- R22 X.Y.Z.62/30
* R21: X.Y.Z.33/3
* R13: X.Y.Z.34/30