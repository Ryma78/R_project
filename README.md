Analyse des Émissions de Gaz à Effet de Serre (GES)
Introduction
Ce notebook R a pour objectif d'analyser les émissions mondiales de gaz à effet de serre (GES) sur une période de plusieurs décennies. L'analyse comprend le nettoyage des données, des statistiques descriptives, des tests d'hypothèse, une régression linéaire et la visualisation des tendances et corrélations.

Source des Données
Les données proviennent du fichier ghg-emissions.csv et contiennent les émissions de GES (en MtCO2e) pour divers pays et régions, de 1990 à 2022.

Préparation et Nettoyage des Données
La première étape cruciale a été le nettoyage et la transformation des données. Cela a inclus :

Le chargement du fichier CSV.
La conversion des colonnes d'années en un format numérique approprié.
Le pivotement des données d'un format large à un format long pour faciliter l'analyse temporelle.
Le filtrage des valeurs manquantes ou non pertinentes.
Le jeu de données final ghg_clean est structuré avec les colonnes Country.Region, Year, et Emissions.

Analyses Réalisées
1. Aperçu des Données et Top 10 Pays
Affichage des 10 premières lignes et des dimensions du jeu de données original.
Calcul et affichage du top 10 des pays par émissions moyennes sur l'ensemble de la période.
2. Visualisation des Top 10 Pays (2010-2022)
Un graphique à barres a été généré pour montrer les 10 pays ayant les émissions moyennes les plus élevées entre 2010 et 2022, offrant une perspective sur les contributeurs récents.
3. Statistiques Descriptives
Calcul des statistiques clés (moyenne, médiane, variance, écart-type, min, max) pour l'ensemble des émissions mondiales.
Un focus a été mis sur la Chine pour analyser ses statistiques spécifiques en tant que leader mondial des émissions.
4. Test de Normalité (Shapiro-Wilk)
Un test de Shapiro-Wilk a été effectué sur un échantillon des données d'émissions pour évaluer si elles suivent une distribution normale. Le résultat a montré que les émissions ne suivent pas une distribution normale.
5. Comparaison des Émissions (Test t de Student)
Une tentative de comparaison des émissions de la Chine et des États-Unis a été faite. Cependant, en raison de données insuffisantes pour les États-Unis sur la période 2010-2022, la comparaison a été réalisée entre la Chine et l'Inde. Le test t de Student a révélé une différence significative entre les émissions moyennes de ces deux pays, avec la Chine ayant des émissions nettement plus élevées.
6. Régression Linéaire pour la Chine
Une régression linéaire a été appliquée aux émissions de la Chine en fonction de l'année pour analyser la tendance temporelle. Le modèle et sa visualisation ont montré une augmentation significative des émissions chinoises sur la période étudiée.
7. Corrélation et Heatmap
(Assumant l'existence de corr_matrix) Une heatmap a été générée pour visualiser les corrélations entre les émissions des cinq principaux pays. Cette visualisation permet d'identifier les relations et les dynamiques entre les émissions des différents acteurs mondiaux.
Résultats Clés
Les données d'émissions mondiales ne suivent pas une distribution normale, ce qui est important pour le choix des méthodes statistiques.
La Chine et les États-Unis sont les plus grands émetteurs, mais la Chine montre une croissance continue.
Une différence significative existe entre les émissions moyennes de la Chine et de l'Inde.
Les émissions de la Chine ont une tendance linéaire positive très forte au fil du temps.
Perspectives Futures
Intégrer d'autres variables (ex: population, PIB) pour une analyse plus approfondie.
Utiliser des modèles de séries temporelles pour la prédiction des émissions futures.
Analyser les émissions par secteur économique ou par continent.
Étudier l'impact des politiques climatiques sur les tendances d'émissions.
