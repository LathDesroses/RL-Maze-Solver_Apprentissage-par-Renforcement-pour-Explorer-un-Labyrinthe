# Introduction to Reinforcement Learning - Projet Labyrinthe

## Description

Ce projet met en œuvre un agent de reinforcement learning utilisant l'algorithme **Q-learning** pour naviguer dans un labyrinthe et atteindre un objectif. L'agent apprend progressivement à éviter les obstacles et à trouver le chemin optimal vers sa destination.

## Fonctionnalités

- **Génération de labyrinthe** : Création d'une grille définissant les chemins possibles et les obstacles.
- **Agent Q-Learning** : Un agent qui apprend à se déplacer en utilisant une table Q.
- **Entraînement et test de l'agent** :
  - **Entraînement** : L'agent est formé sur plusieurs épisodes pour améliorer ses performances.
  - **Test** : Vérification du chemin appris après l'entraînement.
- **Visualisation** : Affichage du labyrinthe et du chemin emprunté par l'agent.

## Installation

Ce projet nécessite **Python 3** et les bibliothèques suivantes :

```bash
numpy matplotlib seaborn tqdm
```

## Utilisation

### 1. Définition du labyrinthe

Le labyrinthe est défini sous forme de tableau NumPy où :

- `0` représente un chemin libre.
- `1` représente un mur.

Exemple :

```python
import numpy as np
maze_layout = np.array([
    [0, 1, 0, 0, 0],
    [0, 1, 1, 1, 0],
    [0, 0, 0, 1, 0],
    [1, 1, 0, 1, 1],
    [0, 0, 0, 0, 0]
])
```

### 2. Création du labyrinthe

```python
maze = Maze(maze_layout, (0, 0), (4, 4))
maze.show_maze()
```

### 3. Entraînement de l'agent

```python
agent = QLearningAgent(maze)
train_agent(agent, maze, num_episodes=100)
```

### 4. Test de l'agent

```python
test_agent(agent, maze)
```

## Exemples de résultats

Avant entraînement :

- Nombre de pas : **79**
- Récompense totale : **-329**

Après entraînement (100 épisodes) :

- Nombre de pas : **8**
- Récompense totale : **93**

## Améliorations possibles

- Implémentation d'une politique epsilon-décroissante plus optimisée.
- Ajout de labyrinthes plus complexes.
- Comparaison avec d'autres algorithmes d'apprentissage par renforcement.

## Auteur

**Lath Essoh**

