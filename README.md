# Olist_brazilian_ecommerce
> Analyse des ventes de la plateforme de e commerce olist

## Analyse n°1
> Quels sont les types de client de la plateforme ?

```python
import pandas as pd
import matplotlib.pyplot as plt

# Créer un histogramme du nombre de clients par type
plt.figure(figsize=(10, 6))
df['lead_type'].value_counts().plot(kind='bar', color='skyblue')
plt.title('Type de clients')
plt.xlabel('Type de lead')
plt.ylabel('Nombre de clients')
plt.xticks(rotation=45)
plt.tight_layout()

# Afficher l'histogramme
plt.show()
```

![Type de client](https://github.com/Aurelie9/Olist_brazilian_ecommerce/assets/161243335/640ffa0b-0bf9-4c80-828d-47e7b3ecbaca)

## Analyse n°2 
> Quels sont les produits les plus vendus sur la plateforme ?

```python
# Créer un histogramme du nombre d'achats par catégorie
plt.figure(figsize=(14, 6))
df['business_segment'].value_counts().plot(kind='bar', color='salmon')
plt.title('Nombre d\'achats par catégorie de produits')
plt.xlabel('Catégorie de produits')
plt.ylabel('Nombre d\'achats')
plt.xticks(rotation=45)
plt.tight_layout()

# Afficher l'histogramme
plt.show()
```

![Type de client](https://github.com/Aurelie9/Olist_brazilian_ecommerce/assets/161243335/1ca149b6-94a0-4d42-bcc7-2ea605ec8883)

## Analyse n°3 
> Quels sont les clients qui contribuent le plus au chiffre d'affaire

```python
# Grouper les données par type de lead et calculer la somme des revenus mensuels déclarés pour chaque groupe
revenu_par_type = df.groupby('lead_type')['declared_monthly_revenue'].sum()

# Créer un graphique à barres pour visualiser le CA par catégories
plt.figure(figsize=(10, 6))
revenu_par_type.plot(kind='bar', color='skyblue')
plt.title('CA par type de client')
plt.xlabel('Type de client')
plt.ylabel('CA')
plt.xticks(rotation=45)
plt.tight_layout()

# Afficher le graphique
plt.show()
```
![CA client](https://github.com/Aurelie9/Olist_brazilian_ecommerce/assets/161243335/c50ba969-bac6-48c0-9698-ef6c68749005)

## Analyse n°4
> Taille moyenne des produits
```python
#Créer un graphique à barres pour visualiser la taille moyenne des produits par catégorie
plt.figure(figsize=(18, 6))
mean_catalog_size.plot(kind='bar', color='orange')
plt.title('Taille moyenne des produits par catégorie')
plt.xlabel('Catégorie')
plt.ylabel('Taille moyenne des produits')
plt.xticks(rotation=45)
plt.tight_layout()

# Afficher le graphique
plt.show()
```
![taille moyenne des produits](https://github.com/Aurelie9/Olist_brazilian_ecommerce/assets/161243335/97b3a49c-b1fe-49f7-9fe9-a1ebbc93103c)
