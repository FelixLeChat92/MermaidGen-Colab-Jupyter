# Script de génération de diagrammes Mermaid

Ce script Python optimisé pour Google Colab et Jupyter Notebook permet de générer des diagrammes Mermaid à partir d'un code Mermaid défini dans la variable `mermaid_code`. Il offre plusieurs fonctionnalités pour visualiser et enregistrer les diagrammes générés.

## Fonctionnalités principales

- Génération d'un lien vers l'éditeur en ligne Mermaid Live pour visualiser et modifier le diagramme
- Génération d'une image SVG haute qualité du diagramme à partir de kroki.io
- Génération d'une image SVG haute qualité du diagramme à partir de mermaid.ink
- Génération d'une image PNG basse qualité du diagramme à partir de mermaid.ink
- Enregistrement des images générées dans le répertoire courant

## Utilisation

1. Définissez votre code Mermaid dans la variable `mermaid_code`
2. Exécutez les cellules de code dans l'ordre suivant :
   - Importation des bibliothèques nécessaires
   - Définition du code Mermaid
   - Génération du lien Mermaid Live (exécution indépendante)
   - Génération de l'image SVG à partir de kroki.io (exécution indépendante)
   - Génération de l'image SVG à partir de mermaid.ink (exécution indépendante)
   - Génération de l'image PNG à partir de mermaid.ink (exécution indépendante)
3. Les liens vers les différentes représentations du diagramme seront affichés dans la sortie, ainsi que les images générées
4. Les images générées seront enregistrées dans le répertoire courant avec des noms de fichiers basés sur une partie de l'URL

## Dépendances

- Python 3
- Bibliothèques Python : base64, sys, json, zlib, IPython.display, requests

## Retour d'expérience

Au cours de mes recherches pour intégrer des diagrammes Mermaid dans des notebooks Jupyter et Google Colab, j'ai rencontré plusieurs difficultés :

- Les API mermaid-filter et mermaid-cli ne fonctionnaient pas de manière native dans ces environnements. Il y avait des conflits de versions avec les dépendances IPython et ipykernel. 

- Les solutions basées sur nb-mermaid nécessitaient d'anciennes versions d'IPython incompatibles avec les kernels récents. De plus, les images générées étaient de qualité médiocre au format PNG.

- L'utilisation de rich pour afficher les diagrammes Mermaid dans Google Colab ne fonctionnait que pour des fichiers Markdown simples, mais pas avec le rendu Mermaid.

Finalement, je me suis inspiré d'anciennes solutions pour Jupyter utilisant l'API en ligne mermaid.ink. Que j'ai adaptées et améliorées pour avoir un code robuste et efficace pour générer et obtenir facilement les images et fichiers nécessaires.

Ce script rassemble ces différentes approches pour offrir une solution fonctionnelle, en attendant une meilleure intégration native de Mermaid dans les notebooks Jupyter et Colab. N'hésitez pas à l'adapter selon vos besoins !
