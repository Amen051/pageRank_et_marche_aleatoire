# 🌐 Démonstrateur PageRank Interactif

> **Projet académique (L3 Informatique)** — Visualisation interactive des marches aléatoires, de la détection des anomalies du Web, de la matrice de Google et de la convergence du PageRank.

---

## 🚀 À propos du projet

Ce démonstrateur a été conçu dans le cadre d'une soutenance orale de Licence 3 Informatique pour vulgariser et illustrer de manière interactive le fonctionnement mathématique et algorithmique de l'algorithme **PageRank** de Google et la marche aléatoire sur un graphe.

L'application permet de manipuler un graphe orienté de $7$ nœuds présentant des anomalies structurelles réelles du Web et de comparer en direct deux approches fondamentales :
1. **L'approche empirique (Marche Aléatoire / Monte-Carlo)** : Simulation dynamique d'un surfeur aléatoire et étude de la fréquence de visite ($\mathcal{O}(1/\sqrt{T})$).
2. **L'approche théorique (PageRank / Méthode des puissances)** : Calcul algébrique de la distribution stationnaire $\pi^*$ garantie par le **théorème de Perron-Frobenius** grâce à la matrice de Google $G$ ($\mathcal{O}(d^k)$).

---

## ✨ Fonctionnalités Clés

* **Architecture visuelle en Split-Screen** : Un panneau de gauche dédié à la manipulation du graphe interactif et un panneau de droite pour les matrices, les simulations et les graphiques de convergence.
* **Graphe Web à 7 nœuds sur-mesure** :
  * Un **nœud puits** ($C$) sans lien sortant (évaporation de probabilité).
  * Un **cycle fermé sans issue** ($D \leftrightarrow E$) alimenté par une entrée depuis $F$ (piège pour le surfeur).
  * Des composantes déconnectées (rupture de l'irréductibilité).
* **Interactivité complète du Graphe** :
  * Déplacement des sommets à la souris (drag-and-drop).
  * Simulation pas à pas ou en continu d'un **surfeur aléatoire** (avec anneau de suivi dynamique).
  * Arcs orientés courbés par courbes de Bézier pour les relations bidirectionnelles ($\leftrightarrow$).
* **Matrice de Google interactive ($G = dP^* + \frac{1-d}{N}E$)** :
  * Ajustement en direct du facteur d'amortissement $d$ via un curseur.
  * Bascule instantanée entre la matrice brute $P$, la matrice corrigée $P^*$ et la matrice de Google $G$ avec mise en surbrillance au survol.
* **Panneau de comparaison des approches (Étape 4)** :
  * Contrôles fins d'avancement : `+1 pas`, `+500 pas`, `+1 itération`, `+10 itérations`.
  * Barres comparatives en temps réel entre fréquence empirique, itérée théorique $\pi^{(k)}$ et limite exacte $\pi^*$.
* **Graphique de complexité et convergence $L_1$ en plein écran (Étape 5)** :
  * Visualisation logarithmique de l'erreur $L_1$ en fonction du nombre d'opérations calculées.
* **Support des thèmes Clair / Sombre** : Bascule instantanée via un bouton dans l'en-tête.
* **Rendu mathématique natif** : Intégration de KaTeX pour l'affichage de toutes les notations scientifiques ($\pi$, $G$, $P^*$, $\mathcal{O}$, etc.).

---

## 🛠️ Installation & Utilisation

Le projet est entièrement contenu dans un **fichier unique** (Single-File Architecture HTML/JS avec Tailwind CSS et KaTeX chargés via CDN), ce qui le rend extrêmement léger et simple à exécuter.

1. **Cloner le dépôt :**
   ```bash
   git clone https://github.com/Amen051/pageRank_et_marche_aleatoire.git
   cd pageRank_et_marche_aleatoire
   ```

2. **Lancer l'application :**
   Aucune compilation, installation de Node.js ou serveur web complexe n'est requis. Ouvrez simplement le fichier `demo_final.html` dans n'importe quel navigateur web moderne (Chrome, Firefox, Safari, Edge) :
   ```bash
   # Sous Linux / macOS
   open demo_final.html
   
   # Sous Windows
   start demo_final.html
   ```

---

## 📚 Structure Pédagogique en 5 Étapes

1. **Graphe & Matrice $P$** : Présentation du graphe à 7 nœuds et construction de la matrice d'adjacence stochastique.
2. **Anomalies du Web** : Mise en évidence des puits, cycles fermés et composantes non connexes empêchant l'ergodicité.
3. **Saut Aléatoire & Matrice $G$** : Correction des lignes nulles et application de la téléportation uniforme pour satisfaire les conditions du théorème de Perron-Frobenius.
4. **Marche Aléatoire vs PageRank** : Simulation empirique (Monte-Carlo) face à la méthode des puissances itérées.
5. **Complexité & Convergence** : Analyse comparative des coûts algorithmiques et de la vitesse de convergence.

---

## 👤 Auteur

* **Amen ATTIOGBE** — *Étudiant en L3 Informatique*
* **Israel KAKANOU** — *Étudiant en L3 Informatique*
* **Paul ALATERRE** — *Étudiant en L3 Informatique*