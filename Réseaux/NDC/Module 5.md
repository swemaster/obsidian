![[Pasted image 20231101100458.png]]

toujours /31, car c'est le seul moyen de ne pas gaspiller
ipv4 a 32 bits
31 bits il reste seulement 1 bit qu'on alloue pour le host id qui sera à 0 ou 1

un sous-réseau peux être subdiviser en allongant le masque

on veut minimiser l'allocation des ressources

![[Pasted image 20231101101328.png]]


-------------
![[Pasted image 20231101101359.png]]

### à faire à la maison
##### voir le prof si bloquer?

entre les routeurs on utilise des masques de /31

on va avoir 3 longueur de masque

on va avoir 4 sous réseaux 

les 3 sous-réseaux entre les routeurs auront un masque de 31


--------
plus les masques sont courts, plus on optimise, les paquets arrivent plus près de leurs destinations

----------------------

![[Pasted image 20231101103649.png]]


![[Pasted image 20231101104111.png]]


![[Pasted image 20231101104425.png]]



TTL nb de routeurs qui peut traverser 

TTL sert à éviter que les paquets tournent en boucle

![[Pasted image 20231101104712.png]]



![[Pasted image 20231101105209.png]]
![[Pasted image 20231101105246.png]]

![[Pasted image 20231101110219.png]]

Les réseaux locaux ne fonctionneraient pas sans ARP

![[Pasted image 20231101110412.png]]
![[Pasted image 20231101110429.png]]
![[Pasted image 20231101110458.png]]

il nous manque l'addr MAC de la cible
on va trouver cet adresse en envoyant un broadcast

le module Ethernet de la station recoit le broadcast
il repond avec un ARP request et envoit l'addr MAC
![[Pasted image 20231101110652.png]]
![[Pasted image 20231101110705.png]]







![[Pasted image 20231101111114.png]]

il y a du padding pour avoir une trame minimale (?)


![[Pasted image 20231101111211.png]]

![[Pasted image 20231101111400.png]]

