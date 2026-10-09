# TP2 — Deep Learning : Image Quality Assessment

Mini-projet en binôme : prédiction de la qualité d'image (MOS) avec PyTorch.

## Installation

Utiliser **Python 3.13** et ouvrir le dossier du projet dans VS Code.

**Windows (PowerShell)** :

```powershell
python -m venv .venv
```

**macOS (Terminal)** :

```bash
python3 -m venv .venv
```

Dans VS Code, ouvrir `TP2_MiniProject_2026.ipynb`, sélectionner l'environnement `.venv` comme noyau (installer `ipykernel` si VS Code le demande), puis **exécuter une fois la première cellule d'installation du notebook**. Elle installe les versions de `requirements.txt` et sélectionne les roues CUDA sur Windows si un GPU NVIDIA est détecté. Le code d'entraînement choisit automatiquement CUDA (NVIDIA), MPS (Mac compatible) ou CPU.

## Données (non stockées dans Git)

Chaque membre télécharge :

- Images KonIQ-10k **512 × 384** : https://database.mmsp-kn.de/koniq-10k-database.html
- Notes MOS (CSV) : https://raw.githubusercontent.com/subpic/koniq/master/metadata/koniq10k_distributions_sets.csv

Créer l'arborescence suivante à la racine du projet :

```text
iqa_data/
├── images/                 # fichiers .jpg
└── train_labels.csv        # renommer le CSV telecharge
```

Le dossier `iqa_data/` et `.venv/` sont exclus du dépôt Git. Garder dans le notebook les chemins relatifs `iqa_data/images` et `iqa_data/train_labels.csv` (avec `/`, compatibles Windows et macOS).
