![[Pasted image 20230920095909.png]]
![[Pasted image 20230920100050.png]]
![[Pasted image 20230920100425.png]]
![[Pasted image 20230920100506.png]]

Si on fait de la télé-médecine on ne voudra pas perdre l'image, il y aura alors un contrat de service.

![[Pasted image 20230920103213.png]]

![[Pasted image 20230920103401.png]]

Plus le temps est grand, plus le nb de paquets est grand

![[Pasted image 20230920103417.png]]
A taux moyen
W temps moyen
X délai moyen

a) N_file = AxW

b) N_transmi = A * X



![[Pasted image 20230920104013.png]]


A_a,A_b,A_c
routeurs A,B,C

L = 150 octets
délai moyen = 10 ms / paquet
A_aL = 1,2 Mbps
A_bL = 1,3 Mbps
A_cL = 1,4 Mbps

Quel est le nombre moyen de paquets?

N = (A_a + A_b + A_c ) x 10 ms
= [(1,2/150x8) + (1,3/150x8) + (1,4/150x8)] x 10 ms

![[Pasted image 20230920104604.png]]
C'est de voir si le pire cas fonctionne, cependant dans la réalité le pire cas ne fonctionne pas.

![[Pasted image 20230920104649.png]]
![[Pasted image 20230920104702.png]]

d = 500 km
c = 100 Mbps
l_paquet = 1080 octets
l_file = 10 000 octets (utilisé en moyenne à 20%)
délai traitement = 100E-6 s

(voir diapos module 3 p. 25)

le délai bout en bout sera la somme des délais

pas besoin de garder beaucoup de chiffres significatifs, 3234 micro seconde = 3 ms.

b)

![[Pasted image 20230920105642.png]]

(voir p. 37 module 3)
![[Pasted image 20230920105831.png]]

traitement non
propagation non
transmission oui
file non, car peu importe ça taille il doit attendre que la file se vide

-----------

Comment on fait pour évaluer les délais si cela varie selon le traffic?
Solution: on utilise un modèle probabiliste

---------

![[Pasted image 20230920110613.png]]

a)

c = 15 Mbps
a = 100 paq/s
l_moy = 1000 octets
F= 100 paq/s x 1000 octets x 8 bits/bytes

C = 45 Mbps - 15 Mbps = 30 Mbps

L = 1000 octets x 8 bits/bytes 

Délai_attente + transmi = L / C-F

Délai_attente = L / C-F - L/C
D_transmi = L/C

![[Pasted image 20230920110952.png]]

![[Pasted image 20230920111105.png]]
























