# Fatura SaaS — Financial Analysis & Monte Carlo Simulation

## Contexte métier
Fatura est une startup SaaS de facturation tunisienne (contexte Startup Act 2018).
Ce projet analyse la robustesse financière du modèle via une simulation Monte Carlo
en faisant varier les deux hypothèses les plus incertaines : le churn et la croissance.

## Problème métier
> "Si le churn et la croissance dévient de nos hypothèses de base,
> est-ce que Fatura survit financièrement ?"

## Outils utilisés
- Python (numpy, pandas, matplotlib)
- Excel (modèle financier 12 mois, 395 formules)
- Google Colab

## Résultats clés
| Scénario | MRR Mois 12 |
|---|---|
| Pessimiste (10% des cas) | 75 339 TND |
| Probable (50% des cas) | 178 527 TND |
| Optimiste (90% des cas) | 280 509 TND |
| Base Fatura | 197 716 TND |

**Conclusion : Fatura survit dans 100% des scénarios simulés.**
Le MRR minimum (75 339 TND) reste au-dessus du seuil de breakeven (32 500 TND).

## Structure du projet
```
├── fatura_monte_carlo.ipynb        # Notebook Python complet
├── Fatura_SaaS_Financial_Model.xlsx  # Modèle Excel
└── README.md
```
## Hypothèses Monte Carlo
- Churn : entre 2% et 8% (benchmark SaaS B2B tunisien — Flat6Labs)
- Croissance MoM : entre 6% et 18% (benchmark MENA early-stage)
- Nombre de simulations : 1 000

## Leçon clé
Le Monte Carlo ne prédit pas l'avenir.
Il mesure la robustesse d'un modèle face à l'incertitude.
