# EquipMatch AI

> **Le bon équipement. Le bon fournisseur. La bonne décision.**

Prototype interactif d'une plateforme B2B qui aide les entreprises à rechercher, comparer et sélectionner des équipements professionnels (énergie, informatique et bureau, industrie), avec une recherche en langage naturel et des recommandations explicables.

**Démo en ligne :** `https://awafallcontact-droid.github.io/EquipMatch_AI/` 

## ⚠️ Avertissement

Ce projet est un **prototype de démonstration**.

- Les produits, marques, prix, fournisseurs et disponibilités sont **fictifs** et ne constituent pas des offres réelles.
- La recherche « IA » repose sur des **règles locales** (mots-clés et extraction de quantité, budget, puissance, localisation). **Aucun LLM n'est connecté.**
- Les formulaires de devis et fournisseur **n'envoient rien** : aucune demande n'est transmise à un fournisseur réel.
- Les scores affichés sont **illustratifs**. Les recommandations ne remplacent pas une expertise technique, une étude de compatibilité ou une validation de sécurité.
- EquipMatch AI ne dispose pas encore de réseau de fournisseurs partenaires.

## Fonctionnalités

- Bannière d'accueil avec recherche intelligente et visuel d'équipements
- Catalogue de 10 produits de démonstration (énergie, informatique et bureau, industrie), avec filtres, tri et fiches détaillées
- Recherche IA locale : détection de la catégorie, quantité, budget, puissance, usage et localisation ; questions de précision si le besoin est flou
- Panneau « Recommandation EquipMatch AI » : raisons, points à vérifier, compromis
- Comparateur de 3 équipements maximum (critères essentiels et secondaires, informations manquantes signalées)
- Formulaires de demande de devis et « Proposer mes équipements » avec validation des champs
- Feuille de route du MVP et questions possibles du jury
- Interface en **français** avec bascule en **anglais**
- Design responsive (ordinateur et smartphone) et thème clair/sombre automatique

## Structure du projet

```
├── index.html   # Structure et textes de la page
├── style.css    # Design et mise en page responsive
├── script.js    # Catalogue, recherche, comparateur, formulaires, traduction
└── README.md
```

Aucune dépendance, aucun build, aucun serveur : le site est entièrement statique. Seule la police *Sora* est chargée depuis Google Fonts (avec police de secours).

## Lancer en local

1. Téléchargez ou clonez le dépôt :
   ```bash
   git clone https://github.com/awafallcontact-droid/EquipMatch_AI.git
   ```
2. Ouvrez `index.html` dans votre navigateur.

## Publier avec GitHub Pages

1. Dans le dépôt, ouvrez **Settings → Pages**.
2. Sous **Branch**, choisissez `main` et le dossier `/ (root)`, puis **Save**.
3. Après 1 à 2 minutes, le site est disponible à l'adresse indiquée.

## Personnaliser

- **Produits :** modifiez le tableau `P` dans `script.js`. Une donnée inconnue se note `null` et s'affiche « Information à confirmer auprès du fournisseur ».
- **Textes bilingues :** les textes statiques utilisent l'attribut `data-en` dans `index.html` ; les textes dynamiques utilisent des paires `[français, anglais]` dans `script.js`.
- **Couleurs :** variables CSS en tête de `style.css` (`--o`, `--ol`, etc.).

## Feuille de route

1. Interroger des responsables achats, des entreprises industrielles et des fournisseurs
2. Sélectionner une catégorie de matériel et constituer un petit catalogue vérifié
3. Développer une première version : recherche, comparaison et demande de devis
4. Tester la recherche en langage naturel et les recommandations IA
5. Mesurer les retours utilisateurs, le gain de temps et l'intérêt commercial
6. Élargir le catalogue après validation

## Licence

À définir par l'auteure du projet (par exemple MIT, ou « Tous droits réservés » si le projet doit rester privé).
