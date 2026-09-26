# ⚡ EMOM 36 — Force & Puissance (PWA)

Une application web minimaliste et ultra-lisible conçue pour rythmer et suivre un entraînement en circuit de **36 minutes** au format **EMOM** (*Every Minute On the Minute*).

L'objectif de ce circuit est de maximiser la **force**, l'**explosivité** et le **développement de la puissance** avec un matériel fixe (barre, poids, rouleau abdo, barre de traction, kettlebell).

---

## 🎯 Concept du Circuit

Plutôt que d'accumuler une fatigue excessive sur de longues séries, le circuit est découpé en **6 exercices de 1 minute** répétés sur **6 tours** (36 minutes au total). 
L'exécution se fait à haute vitesse / intensité pendant 25 à 35 secondes, suivies de 25 à 35 secondes de récupération active avant l'exercice suivant.

### Structure des 6 Exercices (1 min par exo)

1. **Min 1 — Tractions** (3 à 5 reps) · *Tirage vertical & explosivité*
2. **Min 2 — Pompes explosives / Dips** (10 à 12 reps) · *Poussée haut du corps*
3. **Min 3 — Clean & Jerk (25 kg)** (6 à 8 reps) · *Puissance globale & vitesse*
4. **Min 4 — Rouleau Abdos** (8 à 10 reps) · *Gainage fonctionnel profond*
5. **Min 5 — Rowing Buste Penché (25 kg) / Squat Sauté** (8 à 10 reps) · *Tirage horizontal / Explosivité jambes*
6. **Min 6 — Kettlebell Swings** (12 à 15 reps) · *Extension dynamique de hanche*

---

## ✨ Fonctionnalités de l'App

- 🖤 **UI OLED Dark Mode :** Noir pur `#000000`, fort contraste et grands chiffres lisibles à plusieurs mètres sur le plateau de muscu.
- ⏱️ **Timer EMOM Synchronisé :** Compte à rebours par minute + chrono du temps total restant.
- 🔔 **Bips Audio Synthétisés (Web Audio API) :** Alertes sonores à 3, 2, 1 sec avant chaque changement d'exercice (sans dépendance externe).
- 🔄 **Suivi des Tours :** Progression visuelle des 6 étapes par tour avec indicateur du prochain exercice.
- 📱 **Mobile First & PWA :** Conçue pour être installée directement sur l'écran d'accueil d'un smartphone (iOS / Android) et fonctionner hors-ligne.

---

## 🚀 Déploiement

Cette application est un fichier HTML/CSS/JS unique (`index.html`), sans build ni dépendances.

Elle est hébergée sur **Cloudflare Pages** via une intégration continue (CI/CD) automatisée avec ce dépôt GitHub.
