# Analyse des déterminants du type de logement des ménages urbains au Burkina Faso

![header](https://capsule-render.vercel.app/api?type=cylinder\&color=0:16213e,100:0f3460\&height=180\&text=Analyse%20des%20déterminants%20du%20type%20de%20logement%20des%20ménages%20urbains%20au%20Burkina%20Faso\&fontSize=20\&fontColor=ffffff\&desc=Économétrie%20des%20Variables%20Qualitatives%20|%20Régression%20Logistique%20Multinomiale\&descSize=15\&descAlignY=75)

<p align="center">
<img src="https://img.shields.io/badge/Langage-R-276DC3?style=for-the-badge&logo=r&logoColor=white"/>
<img src="https://img.shields.io/badge/Méthode-Économétrie%20des%20variables%20qualitatives-4CAF50?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Modèle-Logit%20Multinomial-FF6600?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Données-EHCVM%202018-0077B5?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Statut-Terminé-success?style=for-the-badge"/>
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# Résumé

Dans un contexte d'urbanisation rapide et de croissance démographique soutenue au Burkina Faso, la compréhension des facteurs qui influencent les choix résidentiels des ménages constitue un enjeu majeur pour les acteurs du secteur immobilier et les décideurs publics.

Ce projet analyse les déterminants du type de logement occupé par les ménages urbains à partir des données de l'Enquête Harmonisée sur les Conditions de Vie des Ménages (EHCVM 2018). L'étude mobilise une approche économétrique basée sur la régression logistique multinomiale afin d'expliquer les différences observées entre plusieurs catégories de logements.

L'analyse combine des variables socioéconomiques, démographiques, géographiques et relatives aux conditions d'habitat. Des techniques avancées de traitement des données ont également été utilisées : ACP, ACM, imputation multiple, validation croisée et diagnostics statistiques complets.

### 🚀 Key Results

✔ Plus de 3 000 ménages urbains analysés

✔ Construction de variables synthétiques par ACP et ACM

✔ Régression logistique multinomiale sur 4 catégories de logements

✔ Pseudo R² de McFadden : **0.393**

✔ Accuracy moyenne en validation croisée : **67.5 %**

✔ Score socioéconomique, qualité du logement et région identifiés comme principaux déterminants

**Compétences mobilisées :** économétrie, analyse statistique multivariée, modélisation multinomiale, ACP, ACM, imputation multiple, validation croisée, aide à la décision.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 📌 Contexte

Le Burkina Faso connaît depuis plusieurs décennies une croissance urbaine rapide accompagnée d'une transformation progressive des formes d'habitat.

Les ménages urbains occupent des logements très diversifiés allant des logements modernes aux habitations traditionnelles en banco. Ces différences reflètent non seulement les conditions économiques des ménages mais également leur situation démographique, leur environnement géographique et leur niveau d'accès aux infrastructures.

Dans ce contexte, l'entreprise fictive **ImmoFaso S.A.** souhaite mieux comprendre les mécanismes qui influencent les choix résidentiels afin d'adapter son offre immobilière aux besoins réels des ménages urbains.

> 💡 Problématique : Quels sont les principaux facteurs socioéconomiques et démographiques qui déterminent le type de logement occupé par les ménages urbains au Burkina Faso ?

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 🎯 Objectifs

* Identifier les déterminants du type de logement des ménages urbains
* Construire des indicateurs synthétiques de confort et de niveau socioéconomique
* Estimer un modèle logit multinomial permettant de prédire le type de logement
* Évaluer la robustesse du modèle à travers plusieurs diagnostics statistiques
* Formuler des recommandations stratégiques pour le secteur immobilier urbain

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 🗂️ Données

| Caractéristique              | Description                  |
| ---------------------------- | ---------------------------- |
| Source                       | EHCVM 2018                   |
| Pays                         | Burkina Faso                 |
| Population cible             | Ménages urbains              |
| Type de données              | Enquête ménages              |
| Variable cible               | Type de logement             |
| Nombre de catégories finales | 4                            |
| Domaine                      | Habitat et conditions de vie |

### Variables retenues

| Variable            | Type            | Rôle                  |
| ------------------- | --------------- | --------------------- |
| `type_logement`     | Qualitative     | Variable cible        |
| `statut_occupation` | Qualitative     | Statut résidentiel    |
| `age_chef`          | Qualitative     | Facteur démographique |
| `taille_menage`     | Quantitative    | Composition du ménage |
| `depenses_menage`   | Quantitative    | Niveau économique     |
| `score_socioeco`    | Synthétique ACM | Position sociale      |
| `niveau_confort`    | Synthétique ACP | Niveau de confort     |
| `qualite_logement`  | Score composite | Qualité de l'habitat  |
| `region_residence`  | Qualitative     | Facteur géographique  |

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 🔬 Méthodologie

```text
Données EHCVM 2018
        │
        ▼
Sélection des ménages urbains
        │
        ▼
Traitement des données
• Détection des valeurs manquantes
• Imputation multiple (MICE)
• Détection des valeurs aberrantes
        │
        ▼
Construction des indicateurs
• ACP → Niveau de confort
• ACM → Score socioéconomique
• Score qualité logement
        │
        ▼
Analyse exploratoire
• Statistiques descriptives
• Corrélations
• V de Cramer
        │
        ▼
Régression Logistique Multinomiale
        │
        ▼
Validation du modèle
• Test LRT
• Pseudo R²
• Validation croisée
• VIF/GVIF
• Analyse des résidus
        │
        ▼
Recommandations opérationnelles
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 🛠️ Stack technique

<p align="center">
<img src="https://img.shields.io/badge/dplyr-Manipulation-276DC3?style=flat-square&logo=r"/>
<img src="https://img.shields.io/badge/feather-Importation-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/mice-Imputation-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/VIM-Données%20manquantes-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/nnet-Logit%20multinomial-FF6600?style=flat-square"/>
<img src="https://img.shields.io/badge/FactoMineR-ACP%20ACM-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/factoextra-Visualisation-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/caret-Validation-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/car-GVIF-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/pscl-PseudoR²-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/pROC-Performance-276DC3?style=flat-square"/>
<img src="https://img.shields.io/badge/corrplot-Corrélation-276DC3?style=flat-square"/>
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 📊 Résultats

## Performance globale du modèle

| Indicateur          |   Valeur |
| ------------------- | -------: |
| AIC                 |   4658.2 |
| LRT                 |  2913.97 |
| p-value             | < 0.0001 |
| Pseudo R² McFadden  |    0.393 |
| Accuracy moyenne CV |   67.5 % |

## Validation croisée

| Fold    | Accuracy |
| ------- | -------: |
| Fold 1  |   65.5 % |
| Fold 2  |   66.3 % |
| Fold 3  |   69.6 % |
| Fold 4  |   68.8 % |
| Moyenne |   67.5 % |

## Diagnostics du modèle

| Diagnostic           | Résultat    |
| -------------------- | ----------- |
| Multicolinéarité     | Absente     |
| GVIF corrigé max     | 1.36        |
| Résidus              | Acceptables |
| Ajustement global    | Bon         |
| Validité statistique | Confirmée   |


<table>
<tr>
<td valign="top" width="50%">

<h3>Performance globale du modèle</h3>

<table>
<tr><th>Indicateur</th><th>Valeur</th></tr>
<tr><td>AIC</td><td>4658.2</td></tr>
<tr><td>LRT</td><td>2913.97</td></tr>
<tr><td>p-value</td><td>&lt; 0.0001</td></tr>
<tr><td>Pseudo R² McFadden</td><td>0.393</td></tr>
<tr><td>Accuracy moyenne CV</td><td>67.5 %</td></tr>
</table>

</td>

<td valign="top" width="50%">

<h3>Validation croisée</h3>

<table>
<tr><th>Fold</th><th>Accuracy</th></tr>
<tr><td>Fold 1</td><td>65.5 %</td></tr>
<tr><td>Fold 2</td><td>66.3 %</td></tr>
<tr><td>Fold 3</td><td>69.6 %</td></tr>
<tr><td>Fold 4</td><td>68.8 %</td></tr>
<tr><td>Moyenne</td><td>67.5 %</td></tr>
</table>

</td>

<td valign="top" width="50%">

<h3>Diagnostic du modèle</h3>

<table>
<tr><th>Diagnostic</th><th>Résultat</th></tr>
<tr><td>Multicolinéarité</td><td>Absente</td></tr>
<tr><td>GVIF corrigé max </td><td>1.36 </td></tr>
<tr><td>Résidus</td><td>Acceptables</td></tr>
<tr><td>Ajustement global</td><td>Bon</td></tr>
<tr><td>Validité statistique</td><td>Confirmée</td></tr>
</table>

</td>
</tr>
</table>

## Visualisations

### Répartition des types de logement

![](img/repartition_type_logement.png)

### Analyse régionale

![](img/type_logement_3plus.png)

### Test de wald

![](img/test_wald.png)


### Importance relative des déterminants

```text
Score socioéconomique     ████████████████████
Qualité logement          ██████████████████
Statut occupation         ████████████████
Région résidence          ██████████████
Niveau confort            ████████████
Dépenses ménage           ██████████
Taille ménage             ████████
Âge du chef               ██████
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 💡 Interprétation économique

### 1. Effet du niveau socioéconomique

Les ménages disposant d'un niveau socioéconomique élevé présentent une probabilité plus forte d'occuper des logements modernes et mieux équipés.

### 2. Effet de la qualité de l'habitat

La qualité des matériaux utilisés pour les murs, les sols et les toitures influence fortement le type de logement observé.

### 3. Effet territorial

Des différences importantes apparaissent entre les régions urbaines, reflétant les disparités de développement économique et d'urbanisation.

### 4. Effet du statut d'occupation

Les comportements résidentiels diffèrent significativement entre propriétaires et locataires, ce qui influence directement le type de logement occupé.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 🌍 Impact

Les résultats peuvent être exploités par :

* Promoteurs immobiliers
* Urbanistes
* Ministère de l'Habitat
* Collectivités territoriales
* Bureaux d'études
* Chercheurs en économie urbaine
* Institutions de développement
* Organisations internationales

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# ⚠️ Limites

* Données limitées à l'année 2018
* Certaines variables socioéconomiques non observées
* Catégories de logement regroupées pour améliorer la robustesse du modèle
* Nature transversale des données
* Absence d'informations détaillées sur les préférences individuelles

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 🧠 Compétences développées

| Domaine            | Compétences                                            |
| ------------------ | ------------------------------------------------------ |
| Économétrie        | Régression logistique multinomiale                     |
| Statistiques       | ACP, ACM, analyses descriptives                        |
| Data Cleaning      | Imputation multiple, traitement des valeurs aberrantes |
| Validation         | Cross-validation, diagnostics statistiques             |
| Analyse de données | Corrélations, V de Cramer, interprétation              |
| Programmation R    | Manipulation, visualisation, modélisation              |
| Aide à la décision | Traduction des résultats en recommandations            |

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 👥 Équipe & Encadrement

## Réalisé par

<table align="center">
<tr>
<td align="center">
<b>NIAMPA Abdoul Fataho</b><br/>
<sub>Licence Analyse Statistique - ISSP</sub>
</td>

<td align="center">
<b>SAWADOGO Pengdwendé Orianne-Aurèle</b><br/>
<sub>Licence Analyse Statistique - ISSP</sub>
</td>

<td align="center">
<b>YAMEOGO Saïdou</b><br/>
<sub>Licence Analyse Statistique - ISSP</sub>
</td>
</tr>
</table>

## Encadrement

<table align="center">
<tr>
<td align="center">
<b>Dr. Boyam Fabrice YAMEOGO</b><br/>
<sub>Économétrie des Variables Qualitatives</sub><br/>
<sub>Université Joseph Ki-Zerbo</sub>
</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 📁 Structure du projet

```text
📦 determinants-logement-burkina/
├── README.md
├── data/
│   └── ehcvm_2018.feather
├── scripts/
│   ├── nettoyage.R
│   ├── construction_indices.R
│   ├── modelisation_multinomiale.R
│   └── validation_modele.R
├── figures/
│   ├── repartition_logements.png
│   ├── analyse_regionale.png
│   ├── cramer_matrix.png
│   └── residus_multinomiaux.png
├── rapport/
│   └── rapport_final.pdf
└── outputs/
    └── resultats_modeles.xlsx
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 📄 Lire le rapport

```markdown
[INSÉRER_IMAGE_PAGE_DE_GARDE]
```

📥 **Rapport complet :**

<p align="center">
        <img width="717" height="903" alt="Capture d&#39;écran 2026-06-20 151804" src="https://github.com/user-attachments/assets/3ff67169-870f-4a3a-8eeb-7b9f8e29e377" />
</p>

[Lire le rapport](rapport.pdf)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

# 📚 Références bibliographiques

* Agresti, A. (2018). *Statistical Methods for the Social Sciences*.
* Hosmer, D., Lemeshow, S. & Sturdivant, R. (2013). *Applied Logistic Regression*.
* Hair, J. et al. (2019). *Multivariate Data Analysis*.
* Greene, W. (2018). *Econometric Analysis*.
* INSD (2021). *Enquête Harmonisée sur les Conditions de Vie des Ménages (EHCVM 2018)*.
* Institut Supérieur des Sciences de la Population (ISSP).

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:4facfe,100:00f2fe&height=3" width="100%"/>

<p align="center">
<sub>Projet réalisé dans le cadre du cours d'Économétrie des Variables Qualitatives — ISSP · Université Joseph Ki-Zerbo · Burkina Faso 🇧🇫</sub>
</p>

![footer](https://capsule-render.vercel.app/api?type=waving\&color=0:16213e,100:0f3460\&height=100\&section=footer)
