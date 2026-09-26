# ⚡ EMOM Force & Puissance (PWA)

Une application web minimaliste et ultra-lisible conçue pour rythmer et suivre un entraînement en circuit au format **EMOM** (*Every Minute On the Minute*).

L'objectif de ce circuit est de maximiser la **force**, l'**explosivité** et le **développement de la puissance** avec un matériel fixe (barre, poids, rouleau abdo, barre de traction, kettlebell).

---

## 🎯 Concept du Circuit

Plutôt que d'accumuler une fatigue excessive sur de longues séries, le circuit est découpé en **6 exercices de 1 minute** répétisés sur **6 tours (36 min)** ou **7 tours (42 min)**.

L'exécution se fait à haute vitesse / intensité pendant 25 à 35 secondes, suivies de 25 à 35 secondes de récupération active. Si vous êtes en forme, l'application permet de **passer manuellement à l'exercice suivant** pour réduire la récupération et battre votre chrono.

### Structure des 6 Exercices (1 min par exo)

1. **Min 1 — Tractions** (3 à 5 reps) · *TIRAGE VERTICAL*
2. **Min 2 — Pompes explosives / Dips** (10 à 12 reps) · *POUSSÉE HAUT DU CORPS*
3. **Min 3 — Clean & Jerk (25 kg)** (6 à 8 reps) · *PUISSANCE GLOBALE*
4. **Min 4 — Rouleau Abdos** (8 à 10 reps) · *GAINAGE PROFOND*
5. **Min 5 — Rowing Buste Penché (25 kg) / Squat Sauté** (8 à 10 reps) · *TIRAGE HORIZONAL / JAMBES*
6. **Min 6 — Kettlebell Swings** (12 à 15 reps) · *CHAÎNE POSTÉRIEURE*

---

## ✨ Nouvelles Fonctionnalités UX & Contrôle

- 🏋️‍♂️ **Indicateur de Tour Géant :** Affichage très visible du tour actuel (`TOUR 1 / 7`) pour une visibilité parfaite à plusieurs mètres.
- ⏭️ **Saut d'Étape Manuel (Fast-Forward) :** Bouton « Suivant » pour enchaîner directement si vous voulez prendre moins de temps de repos.
- ⏱️ **Chrono Réel & Bilan Final :** Si vous allez plus vite que les 36/42 min imparties, l'application enregistre votre temps réel de réalisation et affiche votre gain de temps ainsi que le total de répétitions accomplies.
- ⚙️ **Sélecteur de Format (6 ou 7 Tours) :** Basculez en un clic entre 6 tours (36 min) et 7 tours (42 min) selon votre niveau de forme.
- 🖤 **UI OLED Dark Mode :** Fond noir pur `#000000`, fort contraste et lisibilité maximale sur le plateau de musculation.
- 🔔 **Bips Audio Synthétisés (Web Audio API) :** Alertes sonores à 3, 2, 1 sec avant chaque changement d'exercice (sans fichier externe).
- 📱 **PWA Ready :** Installable sur l'écran d'accueil iOS/Android pour un fonctionnement fluide et 100% hors-ligne.

---

## 🚀 Déploiement

Cette application est contenue dans un fichier unique (`index.html`), sans build ni dépendance.

Mise à jour automatique via **Cloudflare Pages** à chaque commit sur ce dépôt GitHub.
