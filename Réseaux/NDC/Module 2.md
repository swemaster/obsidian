Une trame possède une en-tête (header) et une remorque (trailer)
![[Pasted image 20230919132259.png]]

Problème: Comment on élimine le header et le trailer? Comment on sais où commence et termine les données?

Solution: marqueur
on met 0 6x1 0 au début et à la fin

Problème: what if the data also has 0 6x1 0 in the middle

Solution #2: Le bourrage. 
À chaque fois qu'on a une suite de 5x1 on met automatiquement 0 afin de ne pas accidentellement créer un marqueur.

-------------------------------------
Technique de détection: vérification de la parité
idk what this shit does or how its useful

---------------------
Méthode générale des codes CRC

Le récepteur divide la trame reçue par le même nombre, s'il n'y a pas de reste à la division, le récepteur assume donc qu'il n'y a pas d'erreur

------------

Techniques contrôle de fot:

1. Stop-and-Wait: le receiver informe le sender quand il peut recevoir la prochaine trame
![[Pasted image 20230919133027.png]]

![[Pasted image 20230919133055.png]]
![[Pasted image 20230919133106.png]]
![[Pasted image 20230919133527.png]]
![[Pasted image 20230919134249.png]]

1000 x 5E-6 = 0,005 s = 5 ms
![[Pasted image 20230919133157.png]]
Infos:
réseau = 100 Mbps
trames = 1500 bytes
distance max = 10 km
ack = 0
Calculs:

a)

Délai propagation: 
10 x 5E-6 = 5E-5 s = 0,000 05 s = 0,05 ms = 50 μs

Délai transmission: 
taille trame (bits) / capacité (Mbps)
(1500 x 8 ) bits / 100 Mbps = 120 ms

a = délai propagation / délai transmission
a = 0,00005 s / 0,120 s
a = 0,000 417 s 
a = 417 μs

b)

efficacité normalisé = 1 / (2xa +1)
efficacité normalisé = 1 / (2x0,000 417 + 1)
efficacité normalisé = 0,999 167


---------------------

Cons de Stop-and-Wait: 1 seule trame à la fois
gros cons quand on a des grandes valeurs de a 

Solution: Sliding Window
Pros: +plusieurs trames à la fois





test

test
