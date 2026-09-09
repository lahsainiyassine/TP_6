
Exercice 1 — Système de Dessin de Formes
Ce qui est fait
Définition d'une classe de base Forme et de ses sous-classes spécialisées : Cercle, Rectangle et Triangle.

Chaque forme possède ses dimensions propres et redéfinit la méthode dessiner().

Stockage de ces objets différents au sein d'un même tableau parent Forme[].

Démonstration du polymorphisme : lors du parcours de la boucle, la JVM résout dynamiquement la méthode dessiner() correspondant au type réel de l'objet en mémoire, et non au type de la référence.

https://github.com/user-attachments/assets/6e12b5c2-6c7d-463b-ab88-dd809f42c9ce


Exercice 2 — Gestionnaire de Bibliothèque Multimédia
Ce qui est fait
Modélisation d'une hiérarchie de contenus avec la classe mère Media déclinée en Audio, Video et LiveStream.

Centralisation de la collection dans une classe MediaLibrary utilisant un tableau redimensionnable.

Redéfinition des méthodes lire() et getDuree() pour chaque type de média.

Gestion des flux continus : LiveStream retourne une durée indéterminée (-1), automatiquement filtrée lors du calcul du temps d'écoute total (totalDuration()).






https://github.com/user-attachments/assets/8afff305-9baa-49db-8a96-8d921c9ce1af



Exercice 3 — Gestion RH : Salaires, Abstraction et Génériques
Ce qui est fait
Organisation modulaire du projet en deux packages distincts :

ma.projet : contient la logique de base (Personne), la classe utilitaire et le test.

ma.projet.bean : regroupe les déclinaisons métier des employés (Developpeur et Manager).

Utilisation d'une classe abstraite Personne :

Empêche l'instanciation directe d'une personne générique.

Impose l'implémentation de la méthode abstraite calculerSalaire() dans les sous-classes (+10 % pour un développeur, +30 % pour un manager).

Fournit une méthode concrète affiche() commune à tous.


https://github.com/user-attachments/assets/8bebd05d-052c-4430-8f30-f91bb58cd66e





Exploitation des génériques avec wildcard (List<? extends Personne>) dans Utils.listerPersonnes() : cela autorise le passage de listes de n'importe quel sous-type de Personne de manière totalement sécurisée et réutilisable.
