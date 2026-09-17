# 🌌 Tableau Périodique Complet — Classification Historique & Spectrale

Dashboard interactif en **HTML / CSS / JavaScript** (fichier unique) présentant les **118 éléments chimiques** classés par date de découverte, avec une frise chronologique, une analyse spectrale simulée et un explorateur détaillé.

Thème visuel : **bleu, blanc, rouge** 🇫🇷

---

## 📖 Description

Ce projet est une adaptation libre du dashboard Streamlit « Tableau Périodique Complet » en une application web **autonome**, sans dépendance externe, qui tient dans un seul fichier HTML.

Il permet d'explorer :

- Le tableau périodique complet (18 colonnes, 7 périodes + lanthanides/actinides)
- Les dates de découverte et les découvreurs
- Les grandes époques historiques (Antiquité → Période Moderne)
- Les spectres RGB caractéristiques des éléments
- Des spectres d'émission simulés (raies principales et secondaires)

---

## ✨ Fonctionnalités

- 🧪 **Tableau périodique interactif** — 118 éléments colorés par catégorie chimique, avec info-bulles et clic vers l'explorateur.
- 📅 **Frise chronologique** — Nuage de points « Année de découverte × Numéro atomique », coloré par époque.
- 🏛️ **Vue par époque** — Cartes détaillées regroupées par période historique (Antiquité, Moyen-Âge, Renaissance, Révolution Chimique, Ère Spectroscopique, Période Moderne).
- 🌈 **Analyse spectrale** — Trois onglets : par catégorie, par époque, et comparaison de spectres simulés.
- 🔍 **Explorateur d'éléments** — Fiche complète pour chaque élément : données historiques, propriétés atomiques, données spectrales et spectre simulé.
- 🎛️ **Filtres dynamiques** — Filtrage par époque et par catégorie chimique, options d'affichage.
- 📱 **Responsive** — S'adapte aux écrans mobiles et tablettes.
- 🎨 **Thème tricolore** — Bandeau bleu-blanc-rouge et dégradés aux couleurs de la France.

---

## 🚀 Utilisation

Aucune installation, aucun build, aucune dépendance.

1. Copiez le contenu du fichier HTML dans un fichier nommé `index.html`.
2. Ouvrez ce fichier dans n'importe quel navigateur moderne (Chrome, Firefox, Edge, Safari).
3. C'est tout ! 🎉

```bash
# Exemple : ouvrir directement depuis le terminal
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```
🗂️ Structure du projet

.
├── index.html      # Fichier unique contenant HTML + CSS + JS
└── README.md       # Ce fichier

Le fichier index.html contient :

    HTML : structure de la page (sidebar + contenu principal)

    CSS : styles, thème bleu-blanc-rouge, responsive

    JavaScript : données des 118 éléments, rendu dynamique, graphiques SVG

🎨 Personnalisation

Toutes les données sont centralisées en haut du script JavaScript. Vous pouvez les modifier sans toucher au reste du code.
1. Modifier les éléments

Tableau ELEMENTS :
js

{s:'H', n:'Hydrogène', Z:1, m:1.008, cfg:'1s¹', p:1, g:1,
 cat:'Non-metal', date:1766, dec:'Henry Cavendish', ep:'Révolution Chimique'}

Champ	Description
s	Symbole chimique
n	Nom de l'élément
Z	Numéro atomique
m	Masse atomique (u)
cfg	Configuration électronique
p	Période
g	Groupe
cat	Catégorie chimique
date	Année de découverte (négatif = antiquité)
dec	Découvreur
ep	Époque historique
2. Modifier les spectres

Objet SPECTRAL :
js

'H': {rgb:[255,90,90], wl:656.3, sec:[486.1,434.0], lines:['656.3 nm (Hα)','486.1 nm (Hβ)']}

Champ	Description
rgb	Couleur RGB caractéristique
wl	Longueur d'onde principale (nm)
sec	Raies secondaires (nm)
lines	Libellés des raies principales
3. Modifier les époques

Tableau EPOCHS :
js

{nom:'Antiquité', periode:'Avant 500', bg:'#EFF6FF', border:'#1D4ED8',
 color:'#1E3A8A', point:'#93C5FD', desc:"Éléments connus depuis l'antiquité"}

Vous pouvez renommer, recolori­er ou réordonner les époques.
4. Modifier les couleurs des catégories

Objet CAT_COLORS :
js

'Métal alcalin': '#C8102E',
'Métal de transition': '#1D4ED8',
// etc.

5. Modifier le thème global

Les variables CSS sont définies dans :root :
css

:root{
  --bleu:#002395;
  --rouge:#ED2939;
  --blanc:#ffffff;
  /* ... */
}

📊 Données

Les données historiques et spectrales sont compilées à titre pédagogique et peuvent contenir des approximations. Elles proviennent de sources publiques (Wikipédia, bases de données de spectroscopie, ouvrages de vulgarisation).

    Dates de découverte : les valeurs négatives indiquent une connaissance antique (ex. -25000 pour le carbone).

    Spectres : les longueurs d'onde sont des valeurs caractéristiques simplifiées. Les spectres affichés sont simulés (gaussiennes centrées sur les raies) et non des spectres expérimentaux bruts.

🌐 Compatibilité
Navigateur	Version minimale
Chrome	80+
Firefox	78+
Edge	80+
Safari	14+

Aucune librairie externe n'est requise (pas de React, Vue, D3, Plotly…). Tout est en JavaScript natif et SVG.
📄 Licence

Ce projet est distribué sous licence MIT.

Vous êtes libre de l'utiliser, le modifier et le redistribuer, y compris à des fins commerciales, à condition de conserver la mention de copyright.
text

MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

🙏 Crédits

    Données historiques et spectrales compilées à partir de sources publiques.

    Inspiration : dashboard Streamlit original « Tableau Périodique Complet ».

    Thème visuel : bleu, blanc, rouge — en hommage à la France. 🇫🇷
