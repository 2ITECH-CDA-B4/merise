# Correction exercice 3

---

En considérant tous les attributs proposés ci-après on établit les dépendances fonctionnelles (DF), les dépendances fonctionnelles élementaires et les dépendances fonctionnelles directes (DFD)

***Notre contexte tient compte de tous les attributs ci-après avec les relations données.***

| Relation | DF | DFE | DFR | commentaires |
|:-|:-:|:-:|:-:|:-:|
| 1. (numéro facture, numéro client) -> (nom du client)|X||X|Numéro client suffit à lui tout seul pour obtenir une adresse client donc pas DFE et DFR car rien d'autre d'intermédiaire permet d'avoir le nom du client hormis le numéro client
|2. (numéro facture) -> (adresse client)|X|X||A partir d'une facture on peut obtenir qu'un seul client donc DF. DFE car on a bien à gauche 1 seul attribut. Pas de DFD car on peut passer par numéro client pour obtenir l'adresse du client
|3. (numéro réservation) -> (numéro de chambre)|X|X|X
|4. (numéro de réservation, numéro d'hotel) -> (nom du client)|X|||Pas DFE car numéro réservation suffit à accéder à un seul client et donc à un seul nom. Pas DFD car on peut passer par l'intermédiaire du numéro client
|5. (numéro hotel) -> (nom de la ville)|X|X||1 hotel se trouve dans une seule ville donc connaissant le numéro de l'hôtel, je peux avoir qu'une seule ville et donc son nom. DFE parce qu'un seul attribut à gauche. Pas de DFD car on peut passer par l'intermédiaire de l'identifiant de la ville.
|6. (numéro de service, numéro client) -> (tarif)|X||X|Connaissant le numéro du service on peut accéder à un seul tarif donc DF. Pas DFE car numéro de service suffit à lui tout seul. DFD car on n'a pas d'intermédiaire
|7. (numéro commande, numéro article) -> (nom article)|X||X|Similaire à la 1
|8. (numéro commande, numéro article) -> (quantité commandée)|X|X|X|Il faut à la fois le numéro de commande et d'article pour avoir une seule valeur de la quantité commandé. DFE car les 2 attributs représentent le minimum d'attribut qu'on peut avoir à gauche et DFD car il n' y a pas d'intermédiaire
|9. (numéro commande, numéro client) -> quantité commandée||||Nada pas de DF donc par déduction ni de DFE ni DFD. Effectivement à partir d'un numéro de commande et un numéro client on ne peut pas obtenir la quantité d'un article commandé.
|10. (numéro commande) -> (date de commande)|X|X|X|All in
|11. (numéro commande) -> (nom article)||||Nada pas de DF donc non plus pour les 2 autres