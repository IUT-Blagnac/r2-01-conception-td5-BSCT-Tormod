@startuml

hide circle
hide empty members
hide empty methods

skinparam classAttributeIconSize 0

skinparam roundcorner 5

skinparam class {
    BackgroundColor AliceBluej
    BorderColor DarkSlateGray
    ArrowColor Black
    FontColor Black
    FontSize 12
    FontName Helvetica
}

skinparam arrow {
    MessageAlign center
}

class chantier {
    - String dateDebut
    - String dateFin
    - String adresse
}

class artisant {
    - double salaireH
    - String coordonnee

}

class mission {
    - int nb_heures
    - String debut 
    - String fin 
    - double paie
}

class entreprise {

}

entreprise "1" -- "1.." artisant : Employer
entreprise "1" -- "1.." chantier : Entreprendre
chantier "" -- "" artisant
(chantier,artisant) .. mission

@enduml