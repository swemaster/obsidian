#### | 10^6  | 10^3 | 10^-3 |  10^-6 |
#### | Mega |  Kilo  |   mili   |  micro  |

#### Délai de propagation  = Distance x 5E-6 | (5 μs/km)
#### Délai de transmission (bits)  = Taille_trame / Capacité (bps)

#### a = propagation / transmission
#### w = Taille de la fenêtre (en trames)

![[Pasted image 20231016183629.png]]

T: Taille de la trame en bits
RTT: Délai aller-retour (round trip time)
#### débit max = T/délai = D / RTT


![[Pasted image 20231016184102.png]]
![[Pasted image 20231016191919.png]]
#### w > 2a+1 => il y a transmission continue
#### w < 2a+1 => il n'y a pas transmission continue
#### efficacité normalisée du Sliding Window ne peux être plus grand que 1

W: Taille fenêtre (trames)
#### RTT = 2i + F/C + A/C
#### Efficacité = ( WxD/C ) // RTT

#### Efficacité = D/F
#### Débit max = Efficacité x Capacité 

#### formule du prof:  Capacité de transmission = W * D / RTT
