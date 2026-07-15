# Tic-Tac-Toe - AI Engine (Python/Colab)

Ce dépôt contient l'implémentation complète d'un moteur de jeu **Ultimate Tic-Tac-Toe** (Morpion géant 9x9) doté d'une Intelligence Artificielle basée sur l'algorithme **Minimax avec élagage Alpha-Bêta**.

Ce projet a été conçu pour tourner sur Google Colab et s'affronter lors de tournois académiques à l'ESILV.

---

## Présentation de l'Ultimate Tic-Tac-Toe

L'Ultimate Tic-Tac-Toe est une variante hautement stratégique du Morpion classique :
1. Le plateau géant est composé de **9 sous-grilles** de 3x3.
2. Pour remporter la partie globale, un joueur doit **aligner 3 sous-grilles gagnées** (en ligne, colonne ou diagonale).
3. **La règle de contrainte** : Le coup joué par votre adversaire dans une sous-grille détermine dans quelle sous-grille vous devez obligatoirement jouer au tour suivant. Si cette sous-grille est déjà complétée ou pleine, vous obtenez un "Free Move" (droit de jouer n'importe où).

---

## Caractéristiques de l'IA

L'intelligence artificielle prend des décisions en temps réel (calculées à la volée sous une contrainte stricte de **3 secondes maximum par coup**) :

* **Algorithme de Décision** : Minimax avec élagage Alpha-Bêta pour écarter rapidement les branches de recherche sous-optimales.
* **Gestion Dynamique de la Profondeur** : Ajustement de la profondeur de recherche ($d = 1$, $3$, ou $5$) en fonction de l'avancement de la partie pour optimiser le temps de calcul.
* **Heuristique d'Évaluation Avancée** :
  * Pondération stratégique des cases (le centre macro-board et local offre plus de contrôle).
  * Détection et valorisation des alignements de 2 pions bloqués ou ouverts.
  * Anticipation des coups forcés imposés à l'adversaire.

---

## Structure du Projet

```text
├── Ultimate_TicTacToe.ipynb    # Notebook Google Colab contenant le jeu interactif
└── README.md                   # Présentation du projet
```

## Comment lancer le projet

Importez le fichier ```.ipynb``` dans votre espace Google Colab.

Exécutez la cellule de code principale.

Choisissez l'ordre de jeu (Humain vs IA, IA vs Humain, ou Aléatoire).

Saisissez vos coordonnées de jeu au format ```Ligne Colonne``` (deux chiffres de 1 à 9 séparés par un espace, par exemple : ```4 5```).

