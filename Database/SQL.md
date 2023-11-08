![[Pasted image 20231101155246.png]]

-- afficher le nom et le salaire des employés gagant plus que l'employé #11258 
```sql
select E1.nomemp, E1.salaire
from employé E1, employé E2
where emp2.EMPNO = 11258
and E1.salaire > E2.salaire
```
![[Pasted image 20231101160500.png]]

Éliminer les duplicats

éviter les requêtes imbriquer, elles sont plus longues

![[Pasted image 20231101162151.png]]


