### 1. Doit installer un réseau local dans de nouveaux locaux et vous hésitez entre Ethernet cablée et du Wi-Fi. Comparez les alternatives en faisant une liste d'avantges et incovénients.

Cablé
+ + stable
-  - rend aussi loin que le câble
- - dur de faire passer les fils à travers les murs et les différents étages

WiFi
- - distance limité
- + Faible coût 
- + Flexible
- + Évolutif
- + Scalable
- - Débit plus faible
- - Portée de transmission (mur de béton interfére)
- - Sécurité, plus grand exposition aux risques


### 2. Pourquoi est-il requis d'avoir des ACK dans les réseaux Wi-Fi et non dans les réseaux câblés Ethernet?

Moins de perte dans les réseaux câblés? 

Réseaux câblés plus fiables que réseaux sans-fil.

L'envoi d'un ACK permet au destinataire de confirmer la bonne réception d'un paquet. Si l'émetteur ne reçoit pas d'ACK dans un certain délai, il peut supposer que le paquet a été perdu ou corrompu et le renvoyer si nécessaire.

De plus, les technologies Ethernet utilisent généralement des méthodes telles que la détection de collision (dans le cas des réseaux Ethernet à détection de collision) ou des protocoles de retransmission (comme TCP dans le cas des réseaux TCP/IP) pour gérer les erreurs de transmission. Cela permet de garantir la fiabilité de la communication sans avoir besoin d'ACK explicites.

En résumé, les ACK sont utilisés dans les réseaux Wi-Fi pour compenser les problèmes de fiabilité inhérents à la communication sans fil, tandis qu'ils ne sont pas aussi essentiels dans les réseaux câblés Ethernet en raison de la stabilité généralement supérieure des connexions filaires.

### 3. Quelles sont les fonctions des trames CTS?
RTS : Request to send
CTS : Clear to send

1. Station source envoit un RTS.
2. Destination répond avec un CTS qui donne l'autorisation ou pas d'émettre pendant la durée réservée.
![[Pasted image 20231101085728.png]]

### 4. 
#### a) Quel est l'impact de l'utilisation des ACK sur l'efficacité de la transmission des données?

Garantie la réception

Réduit le débit, car une partie de la bande passante est utilisée pour las transmissions de contrôle plutôt que des données utiles.

Plus grande latence, ACK implique un aller-retour ce qui augmente la latence globale du réseau.

Retransmission, si ACK pas reçu, peut entrainer la duplication des paquets.

===
réponse prof

On arrête pendant un certain temps alors cela ralentit tout
#### b) Faire un exemple, en calculant l'efficacité dans un réseau 802.11ac
DIFS = 34 us
SIFS = 16 us
ACK = 14 octets
tailles données = 500 octets (RTS treshold = 501 octets)
vitesse de transmission = 780 Mbs

(néglige délai de propa et pas d'erreurs)

taille trame données (pas besoin de l'adresse 4 ni du payload) p. 32 Module 4.2 
taille trame = 28

Efficacité = (D / C) // {DIFS + (F/C) + SIFS + (A/C)} 
= 500 x 8 / 780 // 34 + ((520+28)x8)/780 + 16 + (14 x 8)/780
= 9,28 %
#### c) Quel est le débit maximal (en bps) pour transmettre des données dans le réseau 802.11ac sans RTS/CTS
9,28% x C = 9,28% x 780 = 72,38 Mbps

### 5. 
#### a) Quel est l'utilisation du mécanisme RTS/CTS sur l'efficacité de la transmission des données?
Same answer as 4 a)


#### b) 
on se fie à l'image figure 2
eff = (D/C) // ( DIFS + RTS/C + SIFS + CTS/C + SIFS + F/C + SIFS + ACK/C )
eff = 1500x8 / 780 // 34 us + 20x8/780 + 16us + 14x8/780 + 16us + (1500+22)x8/780 + 16us + 19x8/780
eff = 5,83%

#### c) 

780 x 5,83%  = 45,47 Mbps

![[Pasted image 20231101092435.png]]


### 6. 
Réponses dans les NDC
### 7.
Réponses dans les NDC

### 8. Considérant le montage de la figure 3 et que la station H1 passe du BSS 1 au BSS 2. Pourquoi l'AP 2 devrait-il envoyer une trame au commutateur avec l'adresse MAC de la station?

Quand on change de port la table de communication n'est plus bonne alors on doit envoyer une trame afin d'update la table est associé le port à la bonne adresse MAC et éviter de perde des trames.

### 9. 
Réponses dans les NDC

### 10.
#### a)
BSSID
#### b)
p.16 module 5.1
Non, doit rester à l'interne

masque?
classe C 8169/24

#### c) Calculer 
Puissance(dBm) = 10 log_10 (P(w)/lmW)
SNR(dB) = 10log_10  (S(w)/ B(W))
SNR(dB) = -53 dBm -  -94dBm = 41 dB
#### d)
2 spatial streams
-53
780

MCS index 8
400ns
NSS = 2 => 2 spatial streams

