##### Ne pas mettre les unites dans les colonnes 
ex: colonne prix on ne met pas "40$" on met "40"

pour l'examen on etudie jusqu'a la division p.43

### 1 - Affichez la liste des employes dont la date de naissance est entre 2011 et 2013

Employe()

R1 = σ[datedenaissance >= '2011-01-01' AND datedenaissance <= '2011-12-31' 
OR 
datedenaissance >= '2013-01-01' AND datedenaissance <= '2013-12-31'}

Decomposition TP

Employe2011 = σ[datedenaissance >= '2011-01-01' AND datedenaissance <= '2011-12-31' ]
Employe2013 = σ[datedenaissance >= '2013-01-01' AND datedenaissance <= '2013-12-31' ]

R1 = Employe2011 U Employe2013

![[Pasted image 20230927150647.png]]


![[Pasted image 20230927150652.png]]

< ou <=
![[Pasted image 20230927151111.png]]

------------

![[Pasted image 20230927151236.png]]

Relation = Relation (jointure) (condition) 

![[Pasted image 20230927151353.png]]


theta jointure

![[Pasted image 20230927152041.png]]
**On ne met pas de 'theta'**
on met des <, >, <=, >=

![[Pasted image 20230927153230.png]]

F5 est vide alors c'est **NULL**


pi => section des colonnes
