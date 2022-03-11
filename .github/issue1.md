---
title: Exercice 1 : Diagramme des UC en plantUML ({{ date | date('dddd, MMMM Do') }})
---
En vous inspirant du code suivant (pour ne pas démarrer à vide), réalisez un diagramme des UC correspondant au sujet.
```plantuml
@startuml

usecase b as "Gérer ses chentiers"
usecase c as "Gérer ses artisants"
usecase d as "Etre sur un chantier"
usecase e as "Calculer automatiquement la \n paye des employés"

actor Entreprise

'Pour aligner les 2 acteurs :

b -[hidden]-> c
c -[hidden]-> d
d -[hidden]-> e

Entreprise -> b
Entreprise -> c
Entreprise -> d
Entreprise -> e
@enduml
```