
# Calculateur d'Options Black-Scholes avec Grecs et Payoff

Ce script Python permet de calculer le prix d'une option (Call ou Put) en utilisant le modèle de Black-Scholes. Il fournit également les principales "Grecs" (Delta, Gamma, Vega, Theta, Rho) qui mesurent la sensibilité de l'option aux différents facteurs du marché. Enfin, il affiche un graphique interactif du profit/perte net de l'option à l'échéance.

## Fonctionnalités

* **Calcul du prix de l'option** (Call ou Put) selon Black-Scholes.
* Affichage des **paramètres intermédiaires** du modèle (d1, d2, N(d1), N(d2)).
* Calcul et affichage des **Grecs** :
    * **Delta**: Sensibilité du prix de l'option au prix du sous-jacent.
    * **Gamma**: Sensibilité du Delta aux variations du prix du sous-jacent.
    * **Vega**: Sensibilité du prix de l'option à la volatilité du sous-jacent.
    * **Theta**: Dépréciation temporelle du prix de l'option (par jour).
    * **Rho**: Sensibilité du prix de l'option au taux d'intérêt sans risque.
* **Visualisation du Profit/Perte net** à l'échéance via un graphique, incluant le prix d'exercice et le point d'équilibre.

## Prérequis

Assurez-vous d'avoir Python installé sur votre système. Vous aurez également besoin des bibliothèques suivantes :

* `numpy`
* `scipy`
* `matplotlib`

Vous pouvez les installer via pip :

```bash
pip install numpy scipy matplotlib
````

## Exemple d'utilisation

```
Voulez-vous calculer le prix d'une option Call (C) ou Put (P) ? C
Entrez le prix spot actuel (S) : 100
Entrez le prix d'exercice (K) : 110
Entrez le temps jusqu'à l'échéance en années (T) : 0.5
Entrez le taux d'intérêt sans risque (r, ex: 0.045 pour 4.5%) : 0.05
Entrez la volatilité (sigma, ex: 0.2 pour 20%) : 0.2

--- Résultats du Modèle Black-Scholes ---
Le prix de l'option C est : 2.91 $
d1 = -0.4265
d2 = -0.5679
N(d1) = 0.3349
N(d2) = 0.2851

--- Les Grecs ---
Delta = 0.3349
Gamma = 0.0258
Vega = 0.2576 (pour 1% de volatilité)
Theta = -0.0183 (par jour)
Rho = 0.1529 (pour 1% de taux d'intérêt)
```

*(Un graphique s'ouvrira également après ces informations.)*

## Amélioration

A voir...
