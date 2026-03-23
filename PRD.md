# PRD — Melt Landing Page (Hero Section)

## Stack technique

| Outil | Rôle |
|---|---|
| Jekyll | Générateur de site statique, routing multilingue |
| Tailwind CSS v4 | Styling utility-first |
| GSAP | Animations (scroll, entrées, interactions) |
| Unicorn Studio | Background interactif (embed iframe/script) |

---

## Structure Jekyll multilingue

- Une collection par langue : `_i18n/fr/` et `_i18n/en/` (via plugin `jekyll-multiple-languages-plugin`)
- Alternative légère : fichiers `_data/fr.yml` + `_data/en.yml` + prefix de dossier (`/fr/`, `/en/`)
- Langue par défaut : à confirmer (FR ou EN)
- Détection auto : non (switch manuel via nav)

---

## Typographie

**Geist** — Variable font via Google Fonts (wght 100–900)

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Geist:wght@100..900&display=swap" rel="stylesheet">
```

---

## Palette couleurs

| Token | Hex | Notes |
|---|---|---|
| Primary | `#05DAFF` | Cyan vif |
| White | `#F3FDFF` | Blanc légèrement teinté cyan |
| White Alt | dériver de `#F3FDFF` vers primary | Variations UI |
| Black | `#141A1A` | Quasi-noir légèrement chaud |
| Black Alt | dériver de `#141A1A` vers primary | Variations UI |

---

## Assets attendus (à déposer dans `_assets/` une fois le site créé)

| Fichier | Statut |
|---|---|
| Logo SVG (variante choisie) | ⏳ À déposer dans `assets/images/` après init Jekyll |
| Embed Unicorn | ⏳ À fournir (snippet complet) |

---

## Hero Section — Périmètre

- **Layout** : à confirmer (fullscreen / split / centré)
- **Éléments** : logo/navbar, headline, sous-titre, CTA
- **Background** : Unicorn Studio embed (plein écran, derrière le contenu)
- **Animations GSAP** : entrée des éléments (stagger, fade/slide), interaction éventuelle avec le scroll
- **Responsive** : mobile-first, breakpoints Tailwind standard (sm / md / lg / xl)

---

## Langues

- ⏳ À confirmer : FR + EN ? Autres ?
- Contenu hero à fournir dans chaque langue : headline, sous-titre, texte CTA

---

## CTA

- ⏳ Destination à confirmer (Calendly, formulaire, email, page interne)

---

## Contraintes de déploiement

- Site statique exportable (Jekyll build → `_site/`)
- Hébergement cible : à confirmer (Netlify, GitHub Pages, autre)
- Pas de backend / pas de CMS

---

## À faire pour démarrer

1. [x] Confirmer la police (Geist via Google Fonts)
2. [x] Fournir la palette couleurs
3. [ ] Déposer les SVG logo dans `assets/images/` après init Jekyll
4. [ ] Fournir l'embed Unicorn Studio
5. [ ] Confirmer les langues et le contenu hero
6. [ ] Confirmer le layout hero et destination CTA
