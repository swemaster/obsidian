### 1

#### a) Delai de propa ?
infos : 
distance = 1000 km 
vitesse = 5E-6 s/km
reponse: 5 ms

#### b) Delai de transmission pour la telephonie
Combien de fois transmet les trames? 4 fois
Delai de transmission (A1 - > B1) = 4 x delai entre A1 B1

Delai transmi = 4 x 280 x 8 / 100 Mbps = 4 x 22,4 ms = 89,6 ms

#### c) Dans le routeur R1, delai moyen dans la file dattente = ?
Si 10% du traffic est genere par la telephonie.

information non dit: c'est 280-38 octets la taille 

on analyse le delai des paquets

Delai_att+transmi = L / C-F

L: longueur moy des paquets
L = 90%(1580-38 octets) + 10%(280-38 octets)

C = 100 Mbps
F = 95 Mbps

Delai_att = L/C-F - L/C

![[Pasted image 20230927091524.png]]

### 2
Systeme de transmission a *n* noeuds formant une chaine, incluant les hotes sources (noeud 1) et destination (noeud n) Considerez les scenarios A et B
A: un fichier de *M* bits est envoye dans un paquet de noeud 1 au noeud n
B: le fichier est plutot decoupe en p paquets identiques

#### a) Comparez en termes de delai total les scenarios A et B considerant que:
- Delai de propa entre noeuds 1 et n est I (en s)
- taille des trailers et headers est *H+T* (bits)
- delais de traitement et d'attente sont negligeables

A 
1 paquet
taille = M + H + T

Delai A = {M+H+T / C } x (n-1) + I 

Delai B = {( (M/P) + (H+T) )/C } x (n-1) + I + (p-1) x {( (M/P) + (H+T) )/C }


##### Ceci demontre pourquoi on transmet par petits paquets au lieu de tout envoyer d'un coup


![[Pasted image 20230927093516.png]]
![[Pasted image 20230927093522.png]]


#### b) comparez les scenarios A et B en cas d'erreur

### 3 
#### Dans le reseau de la figure 1, des trames sont transmises du routeur A au routeur C. Determinez la capacite minimale du lien entre les routeurs B et C pour que la file d'attente au routeur B utilisee pour la transmission vers C ne deborde pas.

Donnee generales
- Trame de 1000 octets
- Liens bi directionnels
- taille des messages utilises pour les accuses de reception (ACK) est negligeable