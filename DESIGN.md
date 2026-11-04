# La Forge — design contract

## Visual theme & atmosphere
Calme, industriel, précis : fond noir, surfaces presque noires, vert forge comme signal d’action, ambre pour une adaptation. Une seule signature : la progression d’axes de maîtrise.

## Color palette & roles
- `--bg`: `#000000` — canvas
- `--card`: `#09090b` — surface principale
- `--surface`: `#18181b` — contrôles secondaires
- `--text`: `#f4f4f5` — contenu principal
- `--muted`: `#a1a1aa` — aide et contexte
- `--accent`: `#10b981` / `--accent-2`: `#34d399` — action, qualité, progression
- `--amber`: `#f59e0b` — pause, adaptation, intention Défi
- `--rose`: `#f43f5e` — alerte timer, jamais récompense de dépassement

## Typography rules
Space Grotesk pour la lecture et les titres ; JetBrains Mono pour les temps, reps et métadonnées. Les titres restent courts, les actions sont explicites.

## Component stylings
- Cards : bordure discrète, rayon 18–26px, pas d’ombre lourde.
- Actions : cibles tactiles >=44px ; états default/hover/focus-visible/active/disabled.
- Timer : élément dominant pendant la séance.
- Qualité : `Propre`, `Limite`, `Adapter / arrêter` ; aucune action ne pousse à dépasser la forme.

## Layout principles
Mobile-first, largeur de lecture 448px pour l’usage pendant l’effort. Espacement basé sur 4/8/12/16/24/32px. Les axes de La Forge restent lisibles avant les cartes de routines.

## Depth & elevation
Bordures avant ombres. Les cartes utilisent un halo vert très léger uniquement pour signaler une zone active ou une progression.

## Do's and don'ts
- Do : journal local, RIR/effort, variante/charge, note courte, recommandation explicite.
- Do : une surprise optionnelle maximum par séance.
- Don't : leaderboard, punition de streak, hasard sur les mouvements lourds, surcharge de badges, échec musculaire comme objectif.

## Responsive behavior
Routes empilées sur mobile étroit ; aucune information essentielle masquée. `prefers-reduced-motion` désactive les animations. Le focus clavier reste visible.

## Agent prompt guide
Préserver le cœur EMOM et les trois routes `Force`, `Puissance`, `Volume`. Pour toute évolution : privilégier une adaptation sûre et traçable à l’ajout de volume automatique.
