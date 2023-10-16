### Question 1.
a) Appliquer le bourrage de bits vue en classe avec le marqueur 0 111 111 0

à chaque fois qu'on a 5x1 consécutif on ajoute un 0

b) Pour la séquence suivante enlever les bits ajoutés et identifiez les marqueurs 

**on traite juste ce qu'il y a entre les deux marqueurs**

après 5x1 consécutif on enlève un 0
et on enlève les marqueurs
### Question 2.
Considérons le *Sliding Window* entre C1 et C2 sur un canal de communication en duplex.
Quelle est l'efficacité normalisée *Sliding Window*?

infos:
________________________
Délai de transmission = 10 ms
Taille fenêtre = 10 trames
Taille trame = 1500 octets
Distance = 2000 km
_________________________
#### Solution prof
délai propa = 2000 km x 5E-6 = 0,01 s (10 ms)
a = propa/transmission = 10 / 10 = 1

Effi = W / ( 2a + 1 ) = 10 / 2x1 + 1 = 10/3
2a +1 = 3 < w = 10
pas le temps

10 > 3
W > 2a+1 

w > 2a+1 => il y a transmission continue
w < 2a+1 => il n'y a pas transmission continue, donc efficacité norm. = w / 2a+1

efficacité normalisée ne peux être plus grand que 1
**réponse: efficacité normalisée = 1**
### Question 3.
Pour que ce soit fluide on a besoin de 25 images / seconde
infos:
taille image compressée = 10 000 octets
délai aller-retour (RTT) = 50 ms (50E-3 s})
trames: 1000 octets de données vidéo, 1078 octets par trame
débit de 10 Mbps

### formule du prof: Capacité de transmission = W * D / RTT
### a) Est-il possible de transmettre 25 images / seconde si on utilise *Stop-and-Wait*

1) on veut savoir le débit vidéo
25 images/s x 10 paquets x 1000 octets x  8 bits/paquet = 2 Mbps de débit vidéo

2) débit max
Débit max = Taille trame données / délai =1000 octets x 8 bits/octet / 50E-3 s = 160 000 bps
= 160 kbps

On veut transmettre 2 Mbps, mais nous avons 160 kbps. Il sera donc impossible de transmettre 25 images par seconde.

### b) Est-il possible de transmettre 25 images / seconde si on utilise *Sliding Window* avec une fenêtre de 10 trames?

Capacité de transmission = W * D / RTT
C = 10 x 8000 / 50E-3
C = 1,6 Mbps

On veut transmettre 2 Mbps, mais on a seulement 1,6 Mbps. Cela est donc impossible.
### c) Quelle est la taille min pour transmettre 25 images / seconde si on utilise *Sliding Window*

W_min x D / RTT >= 2 Mbps
D = 1000 octets x 8 bits/octets
RTT = 50 ms

W_min x 8000 bits / 50E-3 s >= 2E6 bps
2E6 x 50E-3 / 8000  = 12,5
W_min = 13 

### Question 4. (pas fait)
C1 et C2 distance de 4000 km, communication fait en duplex à 1 Mbps
Trame de 1500 octets
Probabilité d'erreur = 0,25
ACK négligeable

1  / 2a +1 si P_e > 0 => 1-P_e / 2a+1
a) Effica norma = ? si on utilise *Stop-and-Wait* 

b) Effica noma = ? si on utilise Go-Back-N à N retransmissions, considérant W = 10 trames (taille fenêtre)


