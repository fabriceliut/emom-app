# La Forge — design contract

## Visual theme & atmosphere
Calme, industriel, précis : fond noir, surfaces presque noires, vert forge comme signal d’action, ambre pour une adaptation. Une seule signature : la progression d’axes de maîtrise.

## Scenario contract
- **Avant l’effort** : l’utilisateur choisit route, objectif, durée, Maîtrise/Défi, cibles de reps, variantes et charges.
- **Pendant l’effort** : aucun champ texte, nombre ou RIR. Le téléphone est un timer et un feedback.
- **Actions one-tap** : `Fenêtre réussie · X reps`, `Adapter / alléger`, `Passer cette fenêtre`.
- **Automatique** : une fenêtre sans clic est captée comme `auto`, sans inventer de reps.
- **Après l’effort** : le rapport et le journal local sont créés depuis les événements. La note libre est facultative.

## Color palette & roles
- `--bg`: `#000000` — canvas
- `--card`: `#09090b` — surface principale
- `--surface`: `#18181b` — contrôles secondaires
- `--text`: `#f4f4f5` — contenu principal
- `--muted`: `#a1a1aa` — aide et contexte
- `--accent`: `#10b981` / `--accent-2`: `#34d399` — action, qualité, progression
- `--amber`: `#f59e0b` / `--amber-2`: `#fbbf24` — adaptation
- `--rose`: `#f43f5e` — alerte timer, jamais récompense de dépassement

## Typography rules
Space Grotesk pour la lecture et les titres ; JetBrains Mono pour les temps, reps et métadonnées. Les titres restent courts, les actions expliquent immédiatement leur conséquence.

## Component stylings
- Cards : bordure discrète, rayon 18–26px, pas d’ombre lourde.
- Actions : cibles tactiles >=44px ; états default/hover/focus-visible/active/disabled.
- Timer : élément dominant pendant la séance.
- Boutons de séance : espacés, one-tap, `aria-pressed` et région live.
- Timeline : discrète, lisible, non bloquante.

## Layout principles
Mobile-first, largeur de lecture 448px pour l’usage pendant l’effort. Espacement basé sur 4/8/12/16/24/32px. Safe-area iOS conservée. Les axes de La Forge restent lisibles avant les cartes de routines.

## Depth & elevation
Bordures avant ombres. Les cartes utilisent un halo vert très léger uniquement pour signaler une zone active ou une progression.

## Do's and don'ts
- Do : journal local automatique, cibles préparées, variantes/charges préparées, adaptation traçable, rapport depuis événements réels.
- Do : une surprise optionnelle maximum par séance.
- Don't : formulaire pendant l’effort, RIR obligatoire, ressaisie en fin de séance, leaderboard, punition de streak, hasard sur les mouvements lourds, surcharge de badges.

## Responsive behavior
Routes empilées sur mobile étroit ; aucune information essentielle masquée. Le CTA Démarrer reste accessible sur 320/390px. `prefers-reduced-motion` désactive les animations. Le focus clavier reste visible. Contrastes WCAG AA et cibles >=44px.

## Data contract
Chaque fenêtre journalise : exercice, bloc/tour, cible préparée, action, adaptation appliquée, variante/charge, timestamp et statut (`success`, `adapt`, `skip`, `auto`). Les répétitions sont enregistrées uniquement quand l’utilisateur choisit `Fenêtre réussie · X reps`.
