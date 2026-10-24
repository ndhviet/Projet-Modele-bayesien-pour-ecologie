<div align="center">

<h1>Moustique Tigre</h1>

<p><em>Modèle Bayésien Hiérarchique pour la prédiction spatio-temporelle</em></p>

<a href="#"><img src="https://img.shields.io/badge/R-4.5-276DC3?logo=r&logoColor=white&style=flat-square"></a>
<a href="#"><img src="https://img.shields.io/badge/Bayesian-Hierarchical%20Model-orange?style=flat-square"></a>
<a href="#"><img src="https://img.shields.io/badge/Spatio--Temporal-Forecasting-success?style=flat-square"></a>
<a href="#"><img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square"></a>
<a href="#"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square"></a>

<a href="https://ndhviet.github.io/Projet_Modele_hierarchique_bayesien_pour_ecologie/">
  <img src="https://img.shields.io/badge/Demo-Live%20Website-brightgreen?style=for-the-badge&logo=googlechrome&logoColor=white">
</a>


</div>
<br>



<h2 align="center">Réalisé par</h2>

<div align="center">

| Membre | Contact |
|---|---|
| **Duc Hoang Viet NGUYEN** | [ndhviet.github.io](https://ndhviet.github.io/) |
| **Yvan Michel TCHONANG** | [michel-tchonang.lovable.app](https://michel-tchonang.lovable.app/) |

</div>

## 1. Présentation du projet

On s’intéresse dans ce projet à la modélisation de la présence du moustique tigre (*Aedes albopictus*) en France métropolitaine.

Pour cela, on dispose de données d’occurrences du moustique tigre, que l’on peut trouver par exemple sur le site de GBIF (Global Biodiversity Information Facility, [GBIF](https://www.gbif.org/) .

Le but est d’analyser la variabilité inter-site et intra-site des occurrences, en utilisant un modèle hiérarchique bayésien.


## 2. Organisation du projet

- **Partie 1 — Extraction et pré-traitement :** extraction des données, nettoyage des valeurs manquantes et visualisation initiale de la distribution de *Aedes albopictus*.
- **Partie 2 — Modèle hiérarchique bayésien :** deux méthodes ont été testées pour le modèle initial.
  - **Méthode 1 (Part2_1) :** génération par blocs séparés.
  - **Méthode 2 (Part2_2) :** génération du vecteur θ dans son ensemble.
- **Partie 3 — Modèle extension :** reprend la méthode par blocs de la version 1, car l'extension modifie les paramètres de la première partie, ce qui se prête mieux à une approche modulaire.

> **Note importante :** pour que la Méthode 2 fonctionne, le fichier de code doit être placé dans le même répertoire racine que le dossier `data`, afin d'accéder directement à `summary_tigre_moustique.csv`.

## 3. Structure du projet

```text
projet-bayes-moustique/
├── _quarto.yml      # Configuration du site Quarto
├── index.qmd        # Page d'accueil
├── Part1.qmd        # Extraction et pré-traitement
├── Part2_1.qmd      # Génération par blocs
├── Part2_2.qmd      # Génération du vecteur θ
├── Part3.qmd        # Modèle extension
├── Rapport.pdf      # Rapport final
├── data/            # summary_tigre_moustique.csv
├── docs/            # Site web généré
├── images/          # Dashboard
├── model1.png       # Illustrations des modèles
├── model2.png
└── README.md
```

## 4. Consulter le rapport complet

Vous pouvez consulter le rapport détaillé du projet (format PDF) en cliquant sur le lien ci-dessous :

<a href="https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/Rapport.pdf" target="_blank" style="font-weight: bold; text-decoration: underline;">  Ouvrir le rapport PDF  </a>

## 5. Dashboard interactif

[![Dashboard](images/dashboard_bayes.png)](https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/images/dashboard_moustique.html)

➡️ Cliquez sur l'image pour ouvrir le dashboard interactif.

---
