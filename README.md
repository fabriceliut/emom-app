# ⚡ EMOM Force & Puissance (PWA)

Une application web minimaliste et ultra-lisible pour rythmer et suivre un entraînement en circuit au format **EMOM** (*Every Minute On the Minute*).

L'objectif est de développer la **force**, l'**explosivité** et la **puissance** avec un matériel fixe (barre de 25 kg, kettlebell, rouleau abdo, barre de traction, box), en séance de 45 min maximum échauffement compris.

---

## 🎯 Principe

Chaque minute, un exercice. Tu fais tes reps à haute intensité, puis **le temps restant de la minute sert de repos**. C'est ce repos qui garde des reps de qualité d'un tour à l'autre.

Sans charge supplémentaire possible, la progression passe par :

1. **Monter dans la fourchette de reps** jusqu'au haut de la fourchette sur tous les tours.
2. **Passer à une variante plus dure** : tempo lent, pause, unilatéral, déficit.
3. **Garder chaque rep propre**. Sur les exercices de puissance, peu de reps mais explosives.

---

## 🏋️ Routines

Le choix de la routine se fait au lancement de l'app.

### Option A · Force & Puissance (7 tours · 42 min)

| Min | Exercice | Reps | Focus |
|---|---|---|---|
| 1 | Tractions | 3-5 | Tirage vertical |
| 2 | Pompes / Dips | 10-12 | Poussée haut du corps |
| 3 | Clean & Jerk (25 kg) | 6-8 | Puissance globale |
| 4 | Rouleau Abdos | 8-10 | Gainage profond |
| 5 | Box Jump | 10-14 | Puissance des jambes |
| 6 | Kettlebell Swings | 12-15 | Chaîne postérieure |

### Option B · Force unilatérale & Puissance (6 tours · 36 min)

Moins de reps, des variantes plus dures, plus de travail pour les jambes et un tirage horizontal. Les 36 min laissent 7 à 9 min pour l'échauffement.

| Min | Exercice | Reps | Focus |
|---|---|---|---|
| 1 | Box Jump (hauteur max, redescente en marchant) | 4-5 | Puissance des jambes |
| 2 | Tractions tempo (descente en 3 s) | 4-6 | Tirage vertical |
| 3 | Squat bulgare KB (jambe gauche / droite en alternance à chaque tour) | 6-8 | Force unilatérale |
| 4 | Dips / Pompes en déficit (descente en 3 s, pause en bas) | 8-10 | Poussée |
| 5 | Power Clean + Push Press (25 kg) | 5 | Puissance globale |
| 6 | Rows inversés / Roue abdos (en alternance à chaque tour) | 8-10 | Tirage horizontal / Gainage |

---

## ✨ Fonctionnalités

- 📋 **Choix de la routine au lancement** : Option A ou Option B, avec la date de la dernière séance pour chacune.
- 🏋️‍♂️ **Indicateur de tour géant** : `TOUR 1 / 7` lisible à plusieurs mètres, avec une barre de progression sur toute la séance.
- ⏱️ **Minuteur fiable** : basé sur l'heure réelle, il ne prend pas de retard et se recale quand l'écran a été verrouillé.
- ☀️ **Écran toujours allumé** pendant la séance (Wake Lock API).
- 🔔 **Bips audio synthétisés** (Web Audio API) à 3, 2, 1 s avant chaque changement, un son distinct en fin de séance, et des vibrations sur Android.
- 💾 **Reprise de séance** : la progression est sauvegardée. Si tu recharges la page ou reviens au menu, tu peux reprendre là où tu en étais.
- 📈 **Journal des reps** : en fin de séance, tu notes tes reps au dernier tour pour chaque exercice. Pendant la séance suivante, chaque carte affiche « Dernière séance : X reps ».
- ⏭️ **Bouton « Suivant »** : pour corriger une erreur de minute. Le temps réel continue de tourner.
- ↺ **Réinitialisation avec confirmation** pour éviter de perdre une séance sur un mauvais tap.
- 🖤 **UI OLED Dark Mode** : fond noir pur `#000000`, fort contraste, lisible sur le plateau de musculation.
- 📱 **PWA** : installable sur l'écran d'accueil iOS et Android, fonctionne 100 % hors ligne une fois chargée.

> Le journal et la séance en cours sont enregistrés dans le navigateur (`localStorage`), donc propres à chaque appareil.

---

## ➕ Ajouter une routine

Dans `index.html`, copie un bloc du tableau `ROUTINES` et adapte-le :

```js
{
  id: "C",                       // identifiant unique
  name: "Option C",
  title: "Nom de la routine",
  description: "Une ligne d'explication.",
  rounds: 6,                     // le temps total = tours × nombre d'exercices
  exercises: [
    { id: "pullup", tag: "TIRAGE VERTICAL", name: "Tractions", reps: "4-6 REPS", advice: "Conseil d'exécution." },
    // Exercice qui alterne à chaque tour :
    { id: "split-squat", tag: "FORCE UNILATÉRALE", name: "Squat bulgare", reps: "6-8 REPS", advice: "…",
      variants: [{ name: "Squat bulgare · gauche" }, { name: "Squat bulgare · droite" }] }
  ]
}
```

L'`id` de chaque exercice sert au journal : deux variantes avec le même `id` partagent le même historique de reps.

---

## 🚀 Déploiement

Site statique, sans build ni dépendance :

```
index.html            → l'application
sw.js                 → service worker (mode hors ligne)
manifest.webmanifest  → installation PWA
icon.svg              → icône
```

Mise à jour automatique via **Cloudflare Pages** à chaque commit sur ce dépôt GitHub.

⚠️ **À chaque mise à jour de l'app**, incrémente la version du cache dans `sw.js` (`const CACHE = 'emom-v2'` devient `'emom-v3'`). Sinon les téléphones peuvent continuer à afficher l'ancienne version.
