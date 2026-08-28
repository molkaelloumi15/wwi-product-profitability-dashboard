<div align="center">

# 📊 Product & Brand Profitability Dashboard
### Wide World Importers

*Tableau de bord Power BI pour l'analyse de rentabilité produits & marques*

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/status-en%20cours-orange?style=for-the-badge)

</div>

---

## 🎯 Objectif

Ce projet a été réalisé pour renforcer mes compétences en **Business Intelligence** (modélisation de données, DAX, data visualisation), avec une approche orientée décision produit.

> **Problème métier traité :** quels produits et marques faut-il prioriser commercialement, et lesquels génèrent du volume sans réelle rentabilité ?

---

## 🗂️ Source des données

Jeu de données public **Wide World Importers** (base d'exemple Microsoft), structuré en étoile.

| Table | Contenu |
|:---|:---|
| 🧾 `FactSale` | Ventes, quantités, prix, taxes, profit |
| 📦 `DimStockItem` | Produits, marques, catégories |
| 👤 `DimCustomer` | Clients |
| 🌍 `DimCity` | Zones géographiques, territoires de vente |
| 📅 `DimDate` | Calendrier (jour, mois, année, fiscal) |
| 🧑‍💼 `DimEmployee` | Vendeurs |

---

## 🧩 Modèle de données

Schéma en étoile — `FactSale` reliée à 5 dimensions :

```
DimStockItem ─┐
DimCustomer ──┤
DimCity ──────┼── FactSale
DimDate ──────┤
DimEmployee ──┘
```

| Relation | Clé |
|:---|:---|
| FactSale ↔ DimStockItem | `Stock Item Key` |
| FactSale ↔ DimCustomer | `Customer Key` |
| FactSale ↔ DimCity | `City Key` |
| FactSale ↔ DimDate | `Invoice Date Key` → `Date` |
| FactSale ↔ DimEmployee | `Salesperson Key` |


---

## 📐 Mesures DAX

```dax
Total Profit      = SUM(FactSale[Profit])
Total Revenue      = SUM(FactSale[Total Excluding Tax])
Profit Margin %    = DIVIDE([Total Profit], [Total Revenue])
Total Quantity     = SUM(FactSale[Quantity])
```

---

## 📑 Pages du dashboard

- [x] **Vue d'ensemble** — KPI clés, filtrable par année
- [x] **Profitabilité par produit/marque** — Top 10, répartition par catégorie, marge vs volume
- [ ] **Tendances dans le temps** — évolution mensuelle/annuelle
- [ ] **Performance par zone/vendeur** — analyse géographique et commerciale

---

## 💡 Insights clés



---

## 🖼️ Aperçu


---

## 🛠️ Stack technique

`Power BI Desktop` · `Power Query` · `DAX` · `Modélisation en étoile`

---

<div align="center">

**🚧 Projet en cours de construction 🚧**

</div>
