# Présentation PowerPoint - Projet Booki
## Structure simplifiée pour slides visuelles

---

## SLIDE 1 : Page de titre
**Titre :** Intégration HTML/CSS - Projet Booki
**Sous-titre :** Présentation technique
**Auteur :** [Votre nom]
**Date :** [Date de présentation]

---

## SLIDE 2 : Contexte
**Titre :** Le projet en quelques mots

- **Mission** : Intégrer 3 maquettes (Desktop, Tablette, Mobile)
- **Technologies** : HTML5 + CSS3 (Flexbox)
- **Contraintes** : Pas de framework, pas de JavaScript
- **Objectif** : Site responsive et accessible

---

## SLIDE 3 : Structure HTML
**Titre :** Architecture sémantique

```
<header> → Navigation
<main>
  ├─ <section> Hébergements
  ├─ <section> Populaires  
  └─ <section> Activités
<footer>
```

✅ Balises HTML5 sémantiques
✅ Structure logique et accessible

---

## SLIDE 4 : Fonctionnalités
**Titre :** Spécifications implémentées

| Fonctionnalité | Statut |
|----------------|--------|
| Barre de recherche | ✅ |
| Navigation avec ancres | ✅ |
| Cartes cliquables | ✅ |
| Filtres interactifs | ✅ |
| Design responsive | ✅ |

---

## SLIDE 5 : Design System
**Titre :** Charte graphique

**Couleurs :**
- 🔵 Bleu principal : `#0065FC`
- 🔵 Bleu clair : `#DEEBFF`
- ⚪ Gris fond : `#F2F2F2`

**Typographie :**
- Police : Raleway (Google Fonts)
- Poids : 400, 500, 700

**Variables CSS** pour maintenabilité

---

## SLIDE 6 : Flexbox
**Titre :** Mise en page flexible

**Utilisation :**
- Navigation
- Grilles de cartes
- Layout responsive
- Footer

**Avantage :** Code propre sans framework

---

## SLIDE 7 : Responsive Design
**Titre :** 3 breakpoints

| Écran | Largeur | Adaptations |
|-------|---------|-------------|
| 🖥️ Desktop | > 1024px | 3 colonnes, navigation horizontale |
| 📱 Tablette | ≤ 1024px | 2 colonnes, layout adapté |
| 📱 Mobile | < 768px | 1 colonne, navigation verticale |

---

## SLIDE 8 : Navigation
**Titre :** Navigation fixe et adaptative

**Desktop :**
- Horizontale, bordure supérieure

**Mobile :**
- Verticale, bordure inférieure
- Logo centré

**Code :** `position: fixed` + media queries

---

## SLIDE 9 : Système de cartes
**Titre :** Composants réutilisables

**Classe `.card` :**
- Fond blanc
- Border-radius 20px
- Ombre portée

**3 variantes :**
1. Hébergements (image haut)
2. Populaires (image gauche)
3. Activités (image pleine largeur)

---

## SLIDE 10 : Formulaire de recherche
**Titre :** Adaptation mobile

**Desktop :**
```
[📍] [Marseille, France] [Rechercher]
```

**Mobile :**
```
[📍] [Marseille, France] [🔍]
```

Affichage conditionnel via CSS

---

## SLIDE 11 : Conformité
**Titre :** Spécifications respectées

✅ Largeur max 1440px
✅ Desktop First
✅ Code valide W3C
✅ Pas de duplication HTML
✅ Classes réutilisables
✅ Balises sémantiques
✅ Font Awesome intégré

---

## SLIDE 12 : Organisation du code
**Titre :** Structure CSS

```
style.css (717 lignes)
├─ General (variables, reset)
├─ Header (navigation, recherche)
├─ Hébergements
├─ Populaires
├─ Activités
├─ Footer
└─ Media Queries (responsive)
```

**Commentaires** pour chaque section

---

## SLIDE 13 : Défis résolus
**Titre :** Points techniques clés

1. **Ordre mobile** → Flexbox `order`
2. **Navigation responsive** → `flex-direction`
3. **Bouton recherche** → Affichage conditionnel
4. **Grille adaptative** → `flex-wrap` + `flex-basis`

---

## SLIDE 14 : Résultat
**Titre :** Livrables

**Fichiers :**
- `index.html` : 605 lignes
- `css/style.css` : 717 lignes
- Images organisées

**Fonctionnalités :**
- ✅ Responsive complet
- ✅ Navigation fonctionnelle
- ✅ Interactions hover
- ✅ Design fidèle

---

## SLIDE 15 : Conclusion
**Titre :** Bilan

**Objectifs atteints :**
✅ Intégration fidèle
✅ Code maintenable
✅ Respect des contraintes
✅ Site accessible

**Prêt pour :**
- Validation W3C
- Tests utilisateurs
- Intégration backend

---

## SLIDE 16 : Questions
**Titre :** Merci pour votre attention

**Questions ?**

---

## Conseils pour la présentation

### Slides visuelles à ajouter :
1. **Capture d'écran** du site desktop
2. **Capture d'écran** du site mobile
3. **Exemple de code** (structure HTML ou CSS)
4. **Diagramme** de la structure des fichiers

### Points à démontrer :
- Ouvrir le site dans le navigateur
- Redimensionner pour montrer le responsive
- Inspecter le code (DevTools)
- Tester les interactions (hover, liens)

### Timing :
- 1 min par slide environ
- 2-3 min pour la démo live
- 1-2 min pour les questions

