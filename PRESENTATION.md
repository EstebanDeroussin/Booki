# Présentation Projet Booki - Intégration HTML/CSS

## Durée : 15 minutes

---

## SLIDE 1 : Introduction

**Titre : Présentation du projet Booki**

-   **Projet** : Intégration de la maquette Booki
-   **Rôle** : Développeur Front-end - Intégration HTML/CSS
-   **Objectif** : Transformer les maquettes desktop/tablette/mobile en site web responsive
-   **Client** : Booki (plateforme de réservation d'hébergements)

---

## SLIDE 2 : Contexte du projet

**Titre : Les enjeux**

-   **3 maquettes** à intégrer : Desktop (>1024px), Tablette (≥768px), Mobile (<768px)
-   **Approche Desktop First** : développement desktop puis adaptation responsive
-   **Contraintes techniques** :
    -   Pas de framework CSS (Bootstrap, Tailwind)
    -   Pas de préprocesseur (Sass, Less)
    -   Pas de JavaScript
    -   Code valide W3C HTML et CSS
    -   Compatibilité Chrome et Firefox

---

## SLIDE 3 : Structure HTML sémantique

**Titre : Architecture du code HTML**

**Balises sémantiques utilisées :**

-   `<header>` : En-tête avec navigation
-   `<nav>` : Menu de navigation
-   `<main>` : Contenu principal
-   `<section>` : Sections (Hébergements, Activités)
-   `<article>` : Cartes d'hébergements et d'activités
-   `<footer>` : Pied de page

**Points clés :**

-   Structure logique et accessible
-   Séparation claire du contenu
-   Respect des bonnes pratiques SEO

---

## SLIDE 4 : Fonctionnalités implémentées

**Titre : Spécifications fonctionnelles**

✅ **Barre de recherche**

-   Champ de saisie éditable
-   Formulaire structuré
-   Design responsive (texte desktop, icône mobile)

✅ **Navigation**

-   Liens "Hébergements" et "Activités" fonctionnels
-   Ancrage vers les sections correspondantes
-   État actif visuel

✅ **Cartes cliquables**

-   Toute la carte est cliquable (pas seulement le titre)
-   Liens vides avec `href="#"` comme spécifié

✅ **Filtres**

-   4 filtres thématiques (Économique, Familial, Romantique, Nos Pépites)
-   Effet hover avec changement de couleur
-   État actif pour "Nos Pépites"

---

## SLIDE 5 : Approche CSS - Design System

**Titre : Organisation du CSS**

**Variables CSS (Custom Properties) :**

```css
:root {
    --main-color: #0065fc; /* Bleu principal */
    --main-bg-color: #f2f2f2; /* Gris de fond */
    --filter-bg-color: #deebff; /* Bleu clair */
}
```

**Avantages :**

-   Maintenabilité du code
-   Cohérence des couleurs
-   Facilité de modification

**Typographie :**

-   Police Raleway (Google Fonts)
-   Poids : 400, 500, 700
-   Tailles adaptatives selon les breakpoints

---

## SLIDE 6 : Approche CSS - Flexbox

**Titre : Mise en page avec Flexbox**

**Utilisation intensive de Flexbox :**

-   Navigation horizontale
-   Grille de cartes d'hébergements (3 colonnes desktop)
-   Section "Populaires" (verticale desktop, horizontale tablette)
-   Section "Activités" (4 colonnes desktop)
-   Footer responsive

**Exemple clé :**

```css
.hebergements-cards {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
}
```

**Avantages :**

-   Layout flexible et responsive
-   Pas besoin de framework
-   Code propre et maintenable

---

## SLIDE 7 : Responsive Design

**Titre : Adaptation multi-écrans**

**Breakpoints respectés :**

-   **Desktop** : > 1024px (version de base)
-   **Tablette** : ≤ 1024px
-   **Mobile** : < 768px

**Adaptations principales :**

**Tablette (≤1024px) :**

-   Filtres en colonne
-   Hébergements et Populaires en colonne
-   Populaires en ligne (3 cartes)
-   Activités : hauteur réduite

**Mobile (<768px) :**

-   Navigation verticale
-   Bouton recherche avec icône uniquement
-   Filtres sur 2 colonnes
-   Toutes les cartes en pleine largeur
-   Populaires avant Hébergements (ordre inversé)

---

## SLIDE 8 : Détails techniques - Navigation

**Titre : Navigation fixe et responsive**

**Desktop :**

-   Navigation fixe en haut
-   Liens horizontaux avec bordure supérieure au hover/actif
-   Logo à gauche, liens à droite

**Mobile :**

-   Navigation fixe agrandie (144px)
-   Logo centré en haut
-   Liens en pleine largeur avec bordure inférieure
-   Adaptation du margin-top du conteneur principal

**Code clé :**

```css
nav {
    position: fixed;
    top: 0;
    z-index: 1000;
}
```

---

## SLIDE 9 : Détails techniques - Cartes

**Titre : Système de cartes réutilisable**

**Classe `.card` commune :**

-   Fond blanc
-   Border-radius : 20px
-   Ombre portée (drop-shadow)
-   Structure flexible

**Variantes :**

-   **Hébergements** : 3 colonnes, image en haut
-   **Populaires** : Image à gauche (33%), contenu à droite (67%)
-   **Activités** : Image pleine largeur, titre en bas

**Accessibilité :**

-   Attributs `alt` descriptifs
-   `aria-hidden="true"` pour les icônes décoratives
-   Classe `.sr-only` pour le texte masqué (notes)

---

## SLIDE 10 : Détails techniques - Formulaire

**Titre : Barre de recherche adaptative**

**Desktop :**

-   Icône localisation + champ texte + bouton "Rechercher"
-   Bouton avec texte visible

**Mobile :**

-   Même structure mais bouton avec icône uniquement
-   Utilisation de classes `.btn-text` et `.btn-icon`
-   Affichage conditionnel via CSS

**Code :**

```css
.search-group .search-button .btn-text {
    display: none; /* Mobile */
}
.search-group .search-button .btn-icon {
    display: flex; /* Mobile */
}
```

---

## SLIDE 11 : Contraintes respectées

**Titre : Conformité aux spécifications**

✅ **Largeur max** : 1440px avec marges blanches au-delà
✅ **Largeur min** : 320px garantie
✅ **Desktop First** : Code de base desktop, puis media queries
✅ **Pas de duplication HTML** : Un seul HTML pour tous les écrans
✅ **Classes CSS réutilisables** : Pas de duplication inutile
✅ **Code valide** : Prêt pour validation W3C
✅ **Balises sémantiques** : Structure HTML5 complète
✅ **Font Awesome** : Bibliothèque d'icônes intégrée
✅ **Couleurs charte** : Respect strict (#0065FC, #DEEBFF, #F2F2F2)

---

## SLIDE 12 : Points forts du code

**Titre : Qualité et maintenabilité**

**Organisation :**

-   CSS structuré par sections (General, Header, Hébergements, etc.)
-   Commentaires clairs pour chaque section
-   Media queries séparées en fin de fichier

**Bonnes pratiques :**

-   Variables CSS pour les couleurs
-   Classes réutilisables (`.card`, `.section-title`)
-   Flexbox pour tous les layouts
-   `box-sizing: border-box` pour éviter les problèmes de dimensions

**Performance :**

-   Pas de framework lourd
-   CSS optimisé
-   Images optimisées (structure de dossiers claire)

---

## SLIDE 13 : Résultat final

**Titre : Ce qui a été livré**

**Fichiers :**

-   `index.html` : 605 lignes, structure sémantique complète
-   `css/style.css` : 717 lignes, responsive et organisé
-   Images organisées par catégories (hébergements, activités, logo)

**Fonctionnalités :**

-   ✅ Site responsive (desktop, tablette, mobile)
-   ✅ Navigation fonctionnelle
-   ✅ Formulaire de recherche
-   ✅ Filtres avec interactions
-   ✅ Cartes cliquables
-   ✅ Design fidèle aux maquettes

**Compatibilité :**

-   Chrome (dernière version)
-   Firefox (dernière version)

---

## SLIDE 14 : Défis et solutions

**Titre : Points d'attention résolus**

**Défi 1 : Ordre des sections mobile**

-   **Problème** : Populaires doit apparaître avant Hébergements sur mobile
-   **Solution** : Utilisation de `order` en Flexbox

**Défi 2 : Navigation responsive**

-   **Problème** : Passage de horizontale à verticale
-   **Solution** : Changement de `flex-direction` + adaptation des bordures

**Défi 3 : Bouton recherche mobile**

-   **Problème** : Texte "Rechercher" trop long sur petit écran
-   **Solution** : Affichage conditionnel texte/icône via CSS

**Défi 4 : Grille de cartes responsive**

-   **Problème** : 3 colonnes desktop → 1 colonne mobile
-   **Solution** : `flex-wrap` + `flex-basis` adaptatif

---

## SLIDE 15 : Conclusion

**Titre : Bilan du projet**

**Objectifs atteints :**
✅ Intégration fidèle des 3 maquettes
✅ Code propre et maintenable
✅ Respect de toutes les contraintes techniques
✅ Site responsive et accessible

**Compétences démontrées :**

-   Maîtrise du HTML5 sémantique
-   Expertise CSS (Flexbox, Media Queries)
-   Approche Desktop First
-   Attention aux détails (accessibilité, validité)

**Prêt pour :**

-   Validation W3C
-   Tests utilisateurs
-   Intégration backend (futur)

---

## SLIDE 16 : Questions

**Titre : Merci pour votre attention**

**Questions ?**

---

## Notes pour la présentation

### Timing (15 minutes) :

-   Slides 1-3 : 2 min (Introduction et contexte)
-   Slides 4-6 : 4 min (Fonctionnalités et CSS)
-   Slides 7-10 : 5 min (Responsive et détails techniques)
-   Slides 11-13 : 2 min (Conformité et résultat)
-   Slides 14-15 : 1 min (Défis et conclusion)
-   Slide 16 : 1 min (Questions)

### Points à mettre en avant :

1. **Respect strict des spécifications** : Tous les points de la note de synthèse ont été respectés
2. **Code propre** : Organisation claire, commentaires, réutilisabilité
3. **Approche méthodique** : Desktop First, puis adaptation progressive
4. **Attention aux détails** : Accessibilité, sémantique, validité

### Démonstration recommandée :

-   Ouvrir le site dans le navigateur
-   Montrer le responsive (redimensionner la fenêtre)
-   Inspecter le code pour montrer la structure
-   Tester les interactions (hover, liens)


- hebergement et activité le hover doit etre juste fonctionnel pareil pour les filtres 

- sur le marseil france (placeholder)

- deux école (soit c'ets un h1 et h2)
- Ou caler des h1 partout 

- mettre des titre sur les card activité 

- mettre une classe qui met en gris (innactive)

- pas d'accent dan sles classes 

- le alt utilité pour l'accécibilité 

- diapo questions 

- 
