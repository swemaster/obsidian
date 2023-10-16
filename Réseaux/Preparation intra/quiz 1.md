#### 1. Identifiez les réseaux
### LAN
- Interconnecte des terminaux dans une zone géo limitée comme une école, une entreprise, campus.
- Utilise des technos sans-fil
- Offre des débits moins élevés entre les réseaux
### WAN
- Utilise des câbles à paires torsadées catégorie 6,7,8 et des câbles à fibres optiques multimode.
- Couvre une grande zone géo allant jusqu'à la planète entière
- Utilise normalement des câbles de fibres optiques monomode
#### 2. Est-ce que la commutation est adaptée au transport de données?
Non, car la commutation nécessite une réservation au départ et le transport lui ne peux prédire, il ne sait pas dont ce qu'il aura besoin.
#### 3. Quelle est l'utilité du modèle OSI (*Open System Interconnection*)?
Tranformer graduellement les données et les préparer au transport. Optimiser l'interreliabilité entre les couches.
#### 4. Associez les fonctions avec les couches du modèle OSI
- Contient différents protocoles dont les utilisateurs ont besoin.
**Application**
- Offre des services de présentation commune de l'information.
**Présentation**
- Fournit les mécanismes d'ouverture, de fermeture et de gestion des sessions entre les applications.
**Session**
- Transport des segments de bout en bout.
**Transport**
- Routage (acheminement) des paquets dans le réseau en utilisant des adresses logiques.
**Réseau**
- Commutation des trames en utilisant des adresses "physiques".
**Liaison**
- Transmission de bits à l'état brut sous forme numérique ou analogique.
**Physique**

#### 5. Identifiez les symboles
disque avec des flèches : routeur, couche réseau
boîte avec des flèches : commutateur, couche liaison 
grande boîte : serveur, couche application
ordinateur : ordinateur, couche application

#### 6. Est-ce qu'un répéteur Ethernet évite les collisions?
Faux, le répéteur fait juste répéter ce qui est transmis sur les autres ports. Si un de ces ports transmet en même temps que le répéteur, il y aura collision.

#### 7. Quelles sont les différences entre un répéteur, commutateur et routeur

Premièrement, ils sont sur différentes couches,
le répéteur est au niveau physique, (répète un singal électrique alors physique)
le commutateur est au niveau liaison, 
le routeur est au niveau réseau,

Le commutateur peut travailler en duplex tandis que le routeur ne peut pas.
#### 8. Considérons les deux trames Ethernet suivantes (sans les 8 premiers octets). Précisez ce que les valeurs soulignées représentent.

Rappel du format d'une trame:
![[Pasted image 20231016131237.png]]
*sans le PRE

a) 00 B0 8E CD A1 00 |***00 04 75 AA DD 08***| 8D 66 A1 B3 ...

DA: 00 B0 8E CD A1 00
SA: *00 04 75 AA DD 08*

C'est le Source Adress

b) 00 04 75 AA BE 37 | 00 B0 8E 75 1A 00 | ***08 06*** | 00 01 08 00 ...

DA: 00 04 75 AA BE 37
SA: 00 B0 8E 75 1A 00
Type: 08 06

C'est le Type (format du paquet, ce qui permet d'identifier ce qu'il y a à l'intérieur)