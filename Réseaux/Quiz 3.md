1.
a) Appliquer le bourrage de bits vue en classe avec le marqueur 0 111 111 0

à chaque fois qu'on a 5x1 consécutif on ajoute un 0

b) Pour la séquence suivante enlever les bits ajoutés et identifiez les marqueurs 

**on traite juste ce qu'il y a entre les deux marqueurs**

après 5x1 consécutif on enlève un 0
et on enlève les marqueurs

2. Quelle est l'efficacité normalisée *Sliding Window*
infos:
délai propra = 10 ms
2000 km
fenêtre = 10 trames
taille trames = 1500 octets

-------------
Solution prof
----------------------
délai propa = 2000 km x 5E-6 = 0,01 s (10 ms)
délai transmi = 0,01 s (10 ms)
a = 1 

Effi = W / ( 2a + 1 ) = 10 / 2x1 + 1 = 10/3
2a +1 = 3 < w = 10
pas le temps

2a+1  < w => il y a transmission continue
2a+1  > w => il n'y a pas transmission continue, donc efficacité norm. = w / 2a+1

efficacité normalisée ne peux être plus grand que 1


**réponse: efficacité normalisée = 1**

-------------




3. Pour que ce soit fluide on a besoin de 25 images / seconde
infos:
taille image compressée = 10 000 octets
délai aller-retour = 50 ms
trames: 1000 octets de données vidéo, 1078 octets par trame
débit 10 Mbps

a) Est-il possible de transmettre 25 images / seconde si on utilise *Stop-and-Wait*
25 images / s = 25 images x 10 000 octets / image = 250 000 octets/ s
débit = 10 000 000 octets/s 

oui

--------
Solution prof
------------

RTT = road trip time = 50 ms

débit vidéo = 25 images/s x 10 paquets/images x 1000 x 8 bits/paquet = 2 Mbs
efficacité stop and wait = ( D/C ) / ( 2i + F/C + A/C )
débit max = efficacité * débit = D / RTT = 8000 bits/50 ms = 160 kbps

on veut transmettre 2 Mbps
on a 160 kbps

réponse: non

--------------



b) Est-il possible de transmettre 25 images / seconde si on utilise *Sliding Window*
fenêtre = 10 trames

-------------------------------------------
Solution prof
--

comment on sait s'il y a transmission continue

2i + F/C + A/C = RTT

W x F/C >= RTT ? Si oui => il y a transmission continue
10 x (1078x8) / 10 Mbps >= 50 ms
8,624 ms >= 50, non => pas de transmission conitnue

efficacité sliding window pour transmission non continue

effi. = ( W x D/C ) / RTT

débit max = Effi. x Capacité = 10x8000 bits / 50 ms = 1,6 Mbps => impossible de transmettre nos 2 Mpbs

-----------------


c) Quelle est la taille min pour transmettre 25 images / seconde si on utilise *Sliding Window*

-------------
Solution prof
--

W_min x 8000 bits / 50 ms >= 2 Mbps
W_min = 13 

-------------


(exo 4 à faire pour la semaine prochaine)
4. C1 et C2 distance de 4000 km, communication fait en duplex à 1 Mbps
Trame de 1500 octets
Probabilité d'erreur = 0,25

1  / 2a +1 si P_e > 0 => 1-P_e / 2a+1
a)

b)
