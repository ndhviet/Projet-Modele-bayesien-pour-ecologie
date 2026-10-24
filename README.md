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

## Réalisé par

| Membre | Contact |
|---|---|
| **Duc Hoang Viet NGUYEN** | [ndhviet.github.io](https://ndhviet.github.io/) |
| **Yvan Michel TCHONANG** | [michel-tchonang.lovable.app](https://michel-tchonang.lovable.app/) |


# Présentation du projet

On s’intéresse dans ce projet à la modélisation de la présence du moustique tigre (*Aedes albopictus*) en France métropolitaine.

Pour cela, on dispose de données d’occurrences du moustique tigre, que l’on peut trouver par exemple sur le site de GBIF (Global Biodiversity Information Facility, <https://www.gbif.org/>).

Le but est d’analyser la variabilité inter-site et intra-site des occurrences, en utilisant un modèle hiérarchique bayésien.

📄 [Ouvrir le rapport PDF](https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/Rapport.pdf)

Le projet est divisé en plusieurs parties :

-   **Partie 1 :** Extraction des données et pré-traitement

    Cette partie est dédiée à l’extraction des données, au nettoyage des valeurs manquantes et à la visualisation initiale pour comprendre la distribution de *Aedes albopictus*.

-   **Partie 2 :** Construction du modèle hiérarchique bayésien

    Nous avons expérimenté deux méthodes pour l’implémentation du modèle initial :

    -   **Méthode 1 :** Génération par blocs séparés. Elle est présentée dans la version 1.

    -   **Méthode 2 :** Génération du vecteur θ dans son ensemble. Elle est contenue dans la version 2.

        **Note importante :** Pour assurer le bon fonctionnement de cette méthode, il est impératif que le fichier de code soit placé dans le même répertoire racine que le répertoire `data`, afin de permettre l’accès direct au fichier `summary_tigre_moustique.csv`.

-   **Partie 3 :** Modèle extension

    Dans cette partie, nous avons adopté la même méthode que celle utilisée dans la version 1 puisqu’elle demande de modifier les paramètres de la première partie ; la seconde approche, plus modulaire, est la plus adaptée.


## Consulter le rapport complet

Vous pouvez consulter le rapport détaillé du projet (format PDF) en cliquant sur le lien ci-dessous :

<a href="https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/Rapport.pdf" target="_blank" style="font-weight: bold; text-decoration: underline;">  Ouvrir le rapport PDF  </a>

### Dashboard interactif

[![Dashboard](images/dashboard_bayes.png)](https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/images/dashboard_moustique.html)

➡️ Cliquez sur l'image pour ouvrir le dashboard interactif.


<div align="center">
  <h1>Moustique Tigre</h1>
  <p><em>Modèle Bayésien Hiérarchique pour la prédiction spatio-temporelle</em></p>

  <a href="#"><img src="https://img.shields.io/badge/R-4.5-276DC3?logo=r&logoColor=white&style=flat-square"></a>
  <a href="#"><img src="https://img.shields.io/badge/Bayesian-Spatio--Temporal%20Model-orange?style=flat-square"></a>
  <a href="#"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square"></a>
  <a href="https://ndhviet.github.io/Projet_Modele_hierarchique_bayesien_pour_ecologie/">
    <img src="https://img.shields.io/badge/Demo-Live%20Website-brightgreen?style=for-the-badge&logo=googlechrome&logoColor=white">
  </a>
</div>
<br>

## 1. Présentation du projet

Ce projet modélise la présence du moustique tigre (*Aedes albopictus*) en France métropolitaine à partir de données d'occurrences, disponibles par exemple sur [GBIF](https://www.gbif.org/) (Global Biodiversity Information Facility).

L'objectif est d'analyser la variabilité inter-site et intra-site des occurrences à l'aide d'un modèle hiérarchique bayésien.

📄 [Ouvrir le rapport PDF](https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/Rapport.pdf)

---

## 2. Organisation du projet

- **Partie 1 — Extraction et pré-traitement :** extraction des données, nettoyage des valeurs manquantes et visualisation initiale de la distribution de *Aedes albopictus*.
- **Partie 2 — Modèle hiérarchique bayésien :** deux méthodes ont été testées pour le modèle initial.
  - **Méthode 1 (Part2_1) :** génération par blocs séparés.
  - **Méthode 2 (Part2_2) :** génération du vecteur θ dans son ensemble.
- **Partie 3 — Modèle extension :** reprend la méthode par blocs de la version 1, car l'extension modifie les paramètres de la première partie, ce qui se prête mieux à une approche modulaire.

> **Note importante :** pour que la Méthode 2 fonctionne, le fichier de code doit être placé dans le même répertoire racine que le dossier `data`, afin d'accéder directement à `summary_tigre_moustique.csv`.

---

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

---

## 4. Réalisé par

| Membre | Contact |
|---|---|
| **Duc Hoang Viet NGUYEN** | [ndhviet.github.io](https://ndhviet.github.io/) |
| **Yvan Michel TCHONANG** | [michel-tchonang.lovable.app](https://michel-tchonang.lovable.app/) |

---

## 5. Dashboard interactif

[![Dashboard](images/dashboard_bayes.png)](https://ndhviet.github.io/Projet-Modele-bayesien-pour-ecologie/images/dashboard_moustique.html)

➡️ Cliquez sur l'image pour ouvrir le dashboard interactif.
