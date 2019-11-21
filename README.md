<div style="text-align: center">
    <img src="img/criusmm.svg" style="width: 100%; display: inline-block" />
</div>

# Formation en apprentissage machine au CRIUSMM

Ce "répo" github contient le matériel utilisé dans la formation en apprentissage machine organisée par Etienne Dumesnil et Pierre Orban au CRIUSMM à l'automne 2019.

Chaque cours repose sur un notebook *Jupyter* (https://jupyter.org), une application WEB qui permet de créer et de partager des documents contenant du code et d'en visualiser le résultat. Toutes les démonstrations reposent sur *ScikitLearn* (https://scikit-learn.org/), une bibliothèque libre *Python* dédiée à l'apprentissage machine. 

Le matériel (notebooks ```.ipynb``` et documents ```.pdf```) est disponible dans des dossiers séparés pour les 6 sessions théoriques et de démonstration (```cours_1, cours_2, cours_3, cours_4, cours_5 et cours_6```). 

Afin de ne pas requérir des participants à la formation de créer un environnement leur permettant l'exécution fluide des notebooks (anaconda recommandé: https://www.anaconda.com/distribution/), une version interactive est accessible sur *Binder* (https://mybinder.org) en suivant ce lien: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/pnplab/ML_CRIUSMM/master)

Les données utilisées pour tous les exemples proviennent de données simulées (fichier ```/data/sim_data_signature_small.csv``` contenant des données transversales pour 543 patients et 90 contrôles, avec 41 variables) à partir de la banque de données Signature (https://www.banquesignature.ca). *__Il est strictement interdit d'utiliser ces données à d'autres fins que de formation. Toute demande d'accès aux données doit être formulée en bonne et due forme:__* https://www.banquesignature.ca/demande-acces/faire-une-demande-dacces/


## Plan de formation

### Cours 1: Intro à l'apprentissage machine
- Statistiques inférentielles vs apprentissage machine
    - interprétation vs prédiction
    - déduction vs induction
    - biais et variance
- Apprentissage machine supervisé vs non supervisé
    - supervisé: régression vs classification
    - non supervisé: réduction vs regroupement

### Cours 2: Apprentissage machine supervisé - régression 
- Concepts fondamentaux de l'apprentissage machine supervisé
    - Hyperparamètres et régularisation: ridge, lasso et elastic-net
    - Méthodes analytique vs itérative (descente de gradient)
    - Validation (croisée, croisée nichée)

### Cours 3: Apprentissage machine supervisé - classification
- Évaluation: matrice de confusion et courbe "ROC"
- Algorithmes
    - Régression logistique
    - Machines à vecteurs de support (marges dure vs souple, noyaux linéaire vs non linéaire)

### Cours 4: Apprentissage machine supervisé - classification (suite)
- Autres algorithmes
    - Arbres de décision
    - Bagging: forêts aléatoires
    - Boosting de gradient
    - Classification naïve bayésienne
    - K plus proches voisins
- Sélection de caractéristiques
- Classification multi-classes

### Cours 5: Apprentissage machine non supervisé
- Réduction de dimensions
    - Analyse en composantes principales
    - "t-SNE"
- Regroupement
    - K-moyennes
    - Décalage de moyenne
    - "DBSCAN"
    - Modèles de mélange gaussien
    - Modèles hiérarchiques
    - Validation (interne vs externe)
    - Modèles d'ensemble

### Cours 6: Réseaux de neurones (profonds)
<br/>
<br/>

## Ressources additionnelles

### Livres

- *The hundred pages machine learning book* (Burkov, 2019): http://themlbook.com. Version gratuite en ligne, et traduction française disponible sur amazon.

<div>
    <img src="img/book_burkov_fr.svg" style="width: 10%; display: inline-block" />
</div><br/>


- *An introduction to statistical learning with applications in R* (James, Witten, Hastie & Tibshirani, 2014): http://faculty.marshall.usc.edu/gareth-james/ISL/. Version gratuite en ligne.

<div>
    <img src="img/book_james.svg" style="width: 30%; display: inline-block" />
</div><br/>


- *Introduction to machine learning with Python* (Muller & Guido, 2016).

<div>
    <img src="img/book_muller.svg" style="width: 30%; display: inline-block" />
</div><br/>


