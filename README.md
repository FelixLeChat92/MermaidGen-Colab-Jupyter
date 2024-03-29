#EN
# Mermaid Diagram Generation Script

This Python script, optimized for Google Colab and Jupyter Notebook, allows you to generate Mermaid diagrams from Mermaid code defined in the `mermaid_code` variable. It offers several features to visualize and save the generated diagrams.

## Main Features

- Generation of a link to the Mermaid Live online editor to visualize and modify the diagram
- Generation of a high-quality SVG image of the diagram using kroki.io
- Generation of a high-quality SVG image of the diagram using mermaid.ink
- Generation of a low-quality PNG image of the diagram using mermaid.ink
- Saving the generated images in the current directory

## Usage

1. Define your Mermaid code in the `mermaid_code` variable
2. Run the code cells in the following order:
   - Import the necessary libraries
   - Define the Mermaid code
   - Generate the Mermaid Live link (independent execution)
   - Generate the SVG image from kroki.io (independent execution)
   - Generate the SVG image from mermaid.ink (independent execution)
   - Generate the PNG image from mermaid.ink (independent execution)
3. The links to the different representations of the diagram will be displayed in the output, along with the generated images
4. The generated images will be saved in the current directory with filenames based on a part of the URL

## Dependencies

- Python 3
- Python libraries: base64, sys, json, zlib, IPython.display, requests

## Feedback

During my research to integrate Mermaid diagrams into Jupyter and Google Colab notebooks, I encountered several difficulties:

- The mermaid-filter and mermaid-cli APIs did not work natively in these environments. There were version conflicts with the IPython and ipykernel dependencies.

- Solutions based on nb-mermaid required older versions of IPython that were incompatible with recent kernels. Moreover, the generated images were of poor quality in PNG format.

- Using rich to display Mermaid diagrams in Google Colab only worked for simple Markdown files, but not with Mermaid rendering.

Finally, I took inspiration from old solutions for Jupyter using the online mermaid.ink API. I adapted and improved them to have a robust and efficient code to easily generate and obtain the necessary images and files.

This script brings together these different approaches to offer a functional solution, while waiting for better native integration of Mermaid in Jupyter and Colab notebooks. Feel free to adapt it according to your needs!

---
#FR

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
