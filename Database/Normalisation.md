Objectif de la normalisation: Minimiser les redondances, réduire les anomalies de stockage

Quelle colonne devrait-on éliminer?
nomdep
Parce que nom dep n'est pas une cle primaire
et car les utilisateurs sont des humains, ils pourraient faire une faute de frappe et écrire informatic, Informatique, informatique, etc
alors cela évite les anomalies et améliore la cohérence des données.

![[Pasted image 20231004150933.png]]

Le problème est qu'il y a des informations sur les employés et sur les départements.
Cela devrait être séparer en 2 tables. Une pour employé, une pour département.

![[Pasted image 20231004151947.png]]

Réflexivité : A-> A
Transitivité : X->Y et Y->Z alors X->Z
Pseudo-transitivité : X->Y et Y,T->Z alors X,T->Z
Décomposition : X -> Y,Z = X->Y et X->Z
Union : X->Y et X->Z = X -> Y,Z
![[Pasted image 20231004152824.png]]

exemple
![[Pasted image 20231004153236.png]]

	![[Pasted image 20231004153934.png]]
	



