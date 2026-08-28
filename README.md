Product & Brand Profitability Dashboard — Wide World Importers

Tableau de bord Power BI analysant la rentabilité des produits et des marques à partir du jeu de données Wide World Importers (Microsoft).

Contexte et objectif

Ce projet a été réalisé pour renforcer mes compétences en Business Intelligence (modélisation de données, DAX, data visualisation) dans une logique orientée décision produit : identifier quels produits et marques génèrent le plus de profit, et où se situent les opportunités d'optimisation.

Problème métier traité : quels produits/marques faut-il prioriser commercialement, et lesquels génèrent du volume sans réelle rentabilité ?

Source des données

Jeu de données public Wide World Importers (base de données d'exemple Microsoft, format star schema), composé de :

Table	Contenu
FactSale	Table de faits — ventes, quantités, prix, taxes, profit
DimStockItem	Produits, marques (Brand), catégories
DimCustomer	Clients
DimCity	Zones géographiques, territoires de vente
DimDate	Calendrier (jour, mois, année, fiscal)
DimEmployee	Vendeurs
Modèle de données

Schéma en étoile : FactSale est reliée aux 5 dimensions via les clés suivantes :

FactSale[Stock Item Key] ↔ DimStockItem
FactSale[Customer Key] ↔ DimCustomer
FactSale[City Key] ↔ DimCity
FactSale[Invoice Date Key] ↔ DimDate[Date]
FactSale[Salesperson Key] ↔ DimEmployee

(Capture du modèle à ajouter ici une fois finalisée)

Mesures DAX principales
dax
Total Profit = SUM(FactSale[Profit])

Total Revenue = SUM(FactSale[Total Excluding Tax])

Profit Margin % = DIVIDE([Total Profit], [Total Revenue])

Total Quantity = SUM(FactSale[Quantity])
Pages du dashboard
Vue d'ensemble — KPI clés (Total Profit, Total Revenue, Profit Margin %, Total Quantity), filtrable par année
Profitabilité par produit/marque — Top 10 marques par profit, répartition par catégorie, marge vs volume
Tendances dans le temps (à venir) — évolution du profit et de la marge par mois/année
Performance par zone/vendeur (à venir) — analyse géographique et par commercial
Insights clés

(Section à compléter une fois l'analyse terminée — exemple de format :)

La marque X représente X % du profit total pour seulement X % du volume de ventes
Le territoire de vente X affiche la meilleure marge moyenne
...
Technologies utilisées

Power BI Desktop · Power Query · DAX · Modélisation en étoile

Captures d'écran

(À ajouter dans un dossier /screenshots une fois le dashboard finalisé)
