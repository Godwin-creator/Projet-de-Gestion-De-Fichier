# Gestionnaire de Système de Fichiers Virtuel (POO)

Ce projet est une application Java simulant un système de fichiers (fichiers simples et répertoires) avec une interface en ligne de commande (CLI). Réalisé dans le cadre du cours de Programmation Orientée Objet au semestre 3 sous la direction de **M. HOETOWOU**.

##  Fonctionnalités implémentées

L'application supporte les commandes standards suivantes :

* [cite_start]**`ls [nom]`** : Affiche le contenu du répertoire courant ou d'un répertoire spécifique[cite: 10, 14].
* **`cd [nom]`** : Change le répertoire courant. [cite_start]Gère les chemins relatifs, les retours (`..`) et le retour à la racine[cite: 1, 5, 6, 8].
* [cite_start]**`mkdir [nom]`** : Crée un nouveau répertoire (avec vérification d'existence)[cite: 30, 34].
* [cite_start]**`touch [nom]`** : Crée un fichier simple[cite: 35, 39].
* [cite_start]**`cp [source] [dest]`** : Copie récursive de fichiers ou de dossiers complets[cite: 23, 25].
* [cite_start]**`mv [source] [dest]`** : Déplacement de fichiers ou de dossiers (logique de copie puis suppression)[cite: 15, 16].
* **`rm [nom]`** : Suppression d'un élément.
* **`exit`** : Sauvegarde automatique de l'état du système (Sérialisation) et quitte.

## Architecture Technique

Le projet repose sur les concepts avancés de la POO :
* **Héritage et Abstraction** : Utilisation d'une classe abstraite `Fichier` pour `Repertoire` et `FichierSimple`.
* **Polymorphisme** : Gestion uniforme des objets lors de l'affichage ou de la copie.
* **Récursivité** : Implémentation d'une "Copie Profonde" (Deep Copy) pour dupliquer des arborescences entières.
* **Persistance** : Sauvegarde de l'arborescence via la sérialisation Java (`ObjectOutputStream`).

##  Arborescence de démonstration

[cite_start]Le système permet de mettre en place la structure demandée pour le TP[cite: 41, 43]:
```text
Root
├── Documents
│   ├── Autres
│   └── Cours
│       ├── POO
│       │   ├── exercice1.txt
│       │   ├── exercice2.txt
│       │   └── exercice3.txt
│       └── UML
├── Téléchargements
└── Vidéos
