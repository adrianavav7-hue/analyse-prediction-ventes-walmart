# 📊 Analyse et prédiction des ventes

## 📌 Présentation du projet

Ce projet a pour objectif d'analyser les ventes hebdomadaires de 20 magasins Walmart entre 2010 et 2012 afin d'identifier les principaux facteurs associés aux variations des ventes et de construire un modèle permettant de prédire leur évolution.

L'analyse combine une approche exploratoire et de Machine Learning, avec pour objectif de transformer les résultats obtenus en recommandations marketing concrètes.

## 🎯 Objectifs

- Explorer les données de ventes
- Identifier les tendances et la saisonnalité
- Comparer les performances des différents magasins
- Étudier l'influence des variables économiques
- Construire un modèle de prédiction des ventes
- Proposer des recommandations marketing basées sur les résultats

## 📊 Données

Le dataset contient 150 observations et 8 variables. Les variables étudiées sont :

- Weekly sales - ventes hebdomadaires enregistrées le vendredi
- Store - identifiant du magasin
- Date - date de l'observation
- CPI - indice des prix à la consommation, utilisé comme indicateur de l'inflation
- Unemployement - taux de chômage
- Fuel Price - prix du carburant
- Holiday flag - indique si la semaine correspond à une période de vacances ou à un jour férié

## ⚠️ Limites

- Le dataset contient seulement 150 observations 
- Le nombre d'observations varie selon les magasins
- Les périodes couvertes ne sont pas identiques pour tous les magasins
- Certaines périodes de l'année sont sous-représentées
- Absence d'informations concernant les spécificités des magasins

## 🔎 Analyse exploratoire

L'analyse exploratoire met en évidence des différences importantes entre les magasins ainsi qu'une forte variabilité des ventes au cours du temps.

Les données disponibles ne couvrent pas les mêmes périodes pour l'ensemble des magasins. Certaines semaines, voire certains mois, sont absents pour plusieurs magasins, ce qui limite la possibilité de reconstituer une série temporelle complète et d'imputer de manière fiable les dates manquantes.

L'analyse temporelle permet néanmoins d'identifier des périodes de faible activité, notamment en avril, septembre, octobre et novembre, tandis que décembre présente les niveaux de ventes les plus élevés.

L'analyse des performances par magasin permet également d'identifier les magasins dont les ventes hebdomadaires moyennes sont inférieures à 500 000 $, notamment les magasins 3, 5, 9 et 16, ainsi que le magasin 4, qui présente les ventes moyennes les plus élevées.

Enfin, l'analyse met en évidence une association entre les ventes et plusieurs variables économiques, notamment le taux de chômage, le CPI et les périodes de vacances.

## 🤖 Machine learning

La régression linéaire obtient un R² de 0,9259 sur l'ensemble de test.

Les performances sont légèrement améliorées avec le modèle Ridge, qui obtient un R² de 0,9267 ainsi qu'un RMSE inférieur à celui de la régression linéaire.

L'analyse des erreurs de prédiction confirme la légère supériorité de Ridge. Ce modèle est donc retenu comme modèle final.

Les résultats du modèle mettent notamment en évidence l'importance des différences entre les magasins ainsi que des associations entre les ventes et certaines variables économiques, notamment le taux de chômage et le CPI.

## 🚀 Pistes d'amélioration

Afin d'approfondir l'analyse, plusieurs améliorations pourraient être envisagées :

- Disposer de données temporelles couvrant une période complète pour chaque magasin
- Enrichir la base avec des informations spécifiques aux magasins : région, localisation, produits proposés, panier moyen,      profil des clients, etc.
- Ajouter des données relatives aux campagnes marketing et aux promotions
- Analyser les magasins individuellement afin de mieux prendre en compte leurs spécificités

## 💡 Recommandations marketing

Les résultats de l'analyse permettent d'envisager plusieurs actions marketing :

- Stimuler les périodes de faible activité grâce à des promotions ou des offres spécifiques
- Développer des actions de fidélisation pour les magasins les plus performants afin d'augmenter la fréquence d'achat et le panier moyen
- Adapter les campagnes marketing aux spécificités de chaque magasin et à leur clientèle
- Anticiper les périodes de forte ou faible demande grâce à l'analyse de la saisonnalité
- Adapter les offres au contexte économique, notamment lors des périodes caractérisées par une inflation ou un taux de chômage plus élevés
- Mettre en place un dashboard de suivi par magasin afin de suivre les performances et de mesurer l'impact des campagnes marketing