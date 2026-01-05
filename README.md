# Lore Playground Gallery

## Présentation

Galerie d'images dense affichant les créations générées avec Playground. Chaque image peut être agrandie en cliquant dessus pour afficher les métadonnées complètes : prompt, prompt négatif, et seed.

## Fonctionnalités

- **Galerie dense** : Grille compacte d'images miniatures
- **Modal lightbox** : Affichage de l'image en grand avec informations
- **Métadonnées complètes** : Seed, Prompt, Negative Prompt
- **Boutons de copie** : Copier rapidement le prompt, le negative, ou le seed
- **Design gothique minimaliste** : Header noir, effet métallique rose-doré sur "LORE"
- **Responsive** : Fonctionne sur mobile et desktop

## Utilisation

### Déploiement sur Netlify

1. Uploadez le dossier `Lore-Gallery` sur Netlify
2. Le site est automatiquement déployé
3. Aucune configuration supplémentaire requise

### Modification

Les images sont hébergées sur GitHub aux adresses :
- Miniatures : Branches `thumbnails1` à `thumbnails4`
- Images grandes : Branches `Big1` à `Big4`

Le fichier CSV des métadonnées est automatiquement chargé depuis :
`https://raw.githubusercontent.com/T0nt0o/Promptofolio_Lore/main/SERONDA_PROMPTS_V7.csv`

## Structure des fichiers

```
Lore-Gallery/
├── index.html      # Galerie principale
├── manifest.json   # Configuration PWA
└── README.md       # Ce fichier
```

## Métadonnées affichées

- **Model** : Modèle utilisé (Playground v2.5, v3, etc.)
- **Sampler** : Échantillonneur (DPM++ 2M Karras, etc.)
- **Filter** : Filtre appliqué
- **Seed** : Seed de génération (copiable)
- **Prompt** : Prompt principal (copiable)
- **Negative** : Prompt négatif (copiable)

## Technique

- HTML5, CSS3, Vanilla JavaScript
- Chargement CSV via fetch API
- Images GitHub Raw avec CORS activé
- Lazy loading des miniatures
- Pas de dépendances externes

---

*Lore Playground Gallery - Generated with ❤️*
