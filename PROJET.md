# PROJET Moment — vue globale des échanges

À lire par tout bot avant une tâche Moment. Contexte des conversations, pas le code.
Mainteneur : Grok Bot (coordinateur). Les autres bots proposent un ajout à Grok Bot, ils n'éditent pas ce fichier.
Dernière mise à jour : 07/11/2026 ~12 h 20.

## Le projet
- Moment : app Expo/React Native, invitations IRL à Paris (resto, bar, culture, sport). Pas une appli de rencontres.
- Ancien nom : Chance (rebaptisé Moment le 06/10). Sous-titre « Un moment à partager. ». Vert #1B4D3E.
- Porteur : Paolo (Paolove). Il teste lui-même sur Expo Go ; son téléphone fait foi.
- Code : /workspace/chance, GitHub Paopaolove/chance (privé), branche V1 feat/invitation-offer-lots.

## Où trouver quoi
- Dépôt public de cette mémoire : https://github.com/Paopaolove/moment-board
- Règles détaillées (source de vérité) : moment-board/DECISIONS.md
- Règles résumées sur une page : moment-board/REGLES-1-page.md
- Tâches et état : moment-board/TABLEAU.md
- Reprise courte : moment-board/HANDOFF.md (tip, ouvert, owner — lire avant une tâche)
- Écrans de l'app : chance/docs/FEATURE-MAP.md
- Vérification : `npm run verify` (tsc, tests, export web, 6 captures) ; hook pre-push.
- Analyses : /workspace/moment-resume-regles-2026-10-17.md, /workspace/resume-lauren-tan-verification.md, audits chance-audit-2026-10-09.md et audit-moment-fb14e0f.md

## Rôles (depuis le 21/10, fin du mode économie)
- Bot ChatGPT (Codex) : tout le code de Moment, avec npm run verify et push.
- Testeur Moment : QA complète de chaque lot, comme avant le 17/10.
- Dev Moment : arrêté, le code est au bot ChatGPT.
- Grok Bot : coordination, registre DECISIONS.md, ce fichier, contrôle que chaque changement correspond à une décision de Paolo.

## Façon de travailler avec Paolo
- Français, factuel, sans smileys, propositions concrètes. Le contredire quand il se trompe.
- Validation : court texte explicatif puis une carte à cases (une case par proposition). Il répond souvent en texte libre.
- Circuit : brief → vérif registre → go de Paolo → code → vérification → push.
- Toute modification de texte d'écran est signalée avec un avant/après.
- Aucune règle métier changée sans demande. Pas de nouveaux cas limites sans nécessité (leçon du 17/10).
- Push après chaque changement validé, fast-forward seulement. Jamais de force push, jamais de merge de master, éviter 3bcb150.
- Jamais commités : start-tunnel.sh, *.log. Pas de paiement réel, pas de Stripe live, pas de store, pas d'EAS.

## Grandes décisions et leur pourquoi
- 06/10 : rebranding Moment, ton « le moment d'abord, pas un rencard ».
- 07/10 : onboarding réduit à 4 étapes ; photo, téléphone, genre, intérêts demandés plus tard.
- 09/10 : photos de moments passés (profil seulement, accord de toute la table).
- 16/10 : joker, départ « Je quitte la table », motif malaise, signalement confidentiel.
- 17/10 : clôture par l'hôte seulement ; deux clôtures (annonce / fin du moment) ; un moment complet sort du fil.
- 17/10 : signalement séparé de la notation ; 8 catégories ; « abusif » seulement si établi.
- 17/10 : la caution sert contre le no-show, la note ne touche jamais l'argent ; rendue à H+6 par défaut.
- 17/10 : contestation d'un « Pas venu » (24 h, une phrase, revue 7 jours max), gelée en version simple : absences déclarables de H à H+6, une seule déclaration par personne et par moment.
- 17/10 : « Pas pour draguer » retiré du profil.
- 18/10 : présence en confirmation croisée (invité et hôte peuvent dire « je suis présent » et confirmer l’autre), de H−15 à H+6 même après clôture. Pourquoi : ne plus dépendre du seul hôte. Un « Pas venu » contraire ouvre la contestation au lieu d’être refusé.
- 18/10 : caution déjà rendue = acquise ; un désaccord ultérieur ne touche que la sanction. Pourquoi : on ne reprend jamais l’argent.
- 25/10 : carte blanche à Grok Bot pour finir l'app. Décisions du jour : barème hôte « Pas venu » rétabli (1 avertissement, 2e compte fermé) ; partenaire calé sur The Fork (liste à H+30, décocher l'absent, 20 € entiers au lieu, 4 absences en 12 mois) ; annulation à H−1 au lieu de 3 h ; libellés « compte fermé » partout. Pourquoi : simplifier et finir un parcours testable.
- 06/11 : look V1 = Moment Pro (blanc / #F7F7F5 / #111111 / CTA #1F2937, Inter Tight, Fraunces). Pourquoi : Paolo a tranché après comparaison Expo Go des protos.

## Abandonné ou clos
- Brief en 3 points de la version GPT et crédit de moment-gpt-pro : non importés.
- Mission Control (bot tiers d'audit) : écarté pour l'instant (coût d'usage, accès larges).
- « Renaissance » hebdomadaire des bots et dossier OneDrive : écartés.

## Ouvert
- Lot 45 QA : V1 en Expo SDK 58 (`caf2198`, non poussé). Store (24) sur demande.


## Journal (une ligne par jour, ajoutée par Grok Bot)
- 07/11 (~12 h 20) : tip `caf2198` lot 45 (SDK 58) commité localement ; vérif Grok OK (6 fichiers, métier intact) ; QA Testeur.
- 07/11 (~12 h 15) : lot 45 lancé (V1 → Expo SDK 58, sans métier) ; ChatGPT briefé ; tip encore `3854cc6`.
- 07/11 (~7 h 20) : tip `3854cc6` inchangé depuis 23 h 50 la veille ; résumé matinal = lots 43+44 (look Pro + signets).
- 06/11 (~23 h 50) : QA Testeur OK sur `3854cc6` ; lot 44 clos (signets) ; 1147 tests ; bots en pause.
- 06/11 (~23 h 50) : tip `3854cc6` lot 44 (signets) poussé ; 1147 tests déclarés ; QA Testeur.
- 06/11 (~23 h 40) : décision Signets (lot 44) inscrite ; ChatGPT code (carte + liste Profil, pas une demande, personne prévenu, sort si passé/complet).
- 06/11 (~11 h 20) : QA Testeur OK sur `5bee1de` ; lot 43+43b clos (look Pro + cibles 44 px) ; 1126 tests ; bots en pause.
- 06/11 : Paolo préfère Moment GPT Pro comme base visuelle ; look V1 aligné (blanc / #F7F7F5 / #111111 / CTA #1F2937, Inter Tight, Fraunces).
- 01/11 (~8 h 55) : QA Testeur OK sur `1a954c6` ; lot 42 clos ; bots en pause ; suite = Expo Go designs.
- 01/11 (~8 h 50) : tip `1a954c6` lot 42 (toast, 1 sur 1, message définitif) ; 1126 tests ; QA Testeur.
- 01/11 (~8 h 45) : après ban, compteur « 1 sur 1 » (pas 1 sur 4) ; lot 42 = toast + compteur.
- 01/11 (~8 h 42) : action board — toast « Absence retenue » doit mentionner la fermeture temporaire (lot 42 à coder).
- 01/11 (~8 h 35) : QA Testeur OK sur `d625af7` ; lot 41 clos ; bots en pause.
- 01/11 (~8 h 30) : tip `d625af7` lot 41 (fermeture temporaire 1 mois) ; 1111 tests ; QA Testeur.
- 01/11 (~8 h 20) : décision produit — à 4 absences lieu : compte fermé temporairement 1 mois (partout) + date de fin ; une absence encore après → compte fermé définitif. Lot 41 à coder. Tip encore `08f6f0b`.
- 01/11 (7 h 20) : aucun commit ni compte rendu depuis 17 h 55 la veille ; tip `08f6f0b` inchangé ; résumé matinal = lots 39+40.
- 31/10 (~17 h 55) : QA Testeur OK sur `08f6f0b` ; lot 40 clos ; bots en pause.
- 31/10 (~17 h 50) : tip `08f6f0b` lot 40 (note neutre, Moments passés Caution, drop counts) ; QA Testeur.
- 31/10 (~17 h 20) : QA Testeur OK sur `24a1da1` ; lot 39 clos ; bots en pause.
- 31/10 (~17 h 20 Europe/Paris) : tip `24a1da1` lot 39 (bandeau Caution + N/4) ; audit OK hors 3 questions Paolo ; QA Testeur.
- 31/10 (~17 h Europe/Paris) : décisions produit — bandeau Caution pas à vie (moment + historique) ; compteur lieu « N sur 4 » privé, 12 mois, 4 = compte fermé. Lot 39 → ChatGPT.
- 17/10 : gros lot caution/contestation/signalement ; bascule vers le bot ChatGPT ; mode économie à 21 h 33 ; outils de vérification livrés.
- 18/10 : création de ce fichier ; présence en confirmation croisée validée et poussée (4383820) ; règle « caution rendue = acquise » validée, code non commité.
- 19/10 et 20/10 : aucune activité Moment visible (ni commit ni fichier modifié) ; résumé du 20/10 en échec.
- 21/10 : fin du mode économie ; retour à l'organisation d'avant, le code reste au bot ChatGPT. Aucun commit ni fichier Moment modifié ; le code « caution rendue = acquise » est toujours non commité.
- 22/10 : aucun commit ni compte rendu de bot ; une vérification (npm run verify) a tourné à 19 h 50 sur le code non commité « caution rendue = acquise » : OK, tsc 0, 759/759 tests, 6 captures.
- 23/10 : aucun commit, aucun fichier Moment modifié, aucun compte rendu de bot ; le code « caution rendue = acquise » attend toujours le contrôle de Paolo sur Expo Go.
- 24/10 : aucun commit, aucun fichier Moment modifié, aucun compte rendu de bot ; le code « caution rendue = acquise » attend toujours le contrôle de Paolo sur Expo Go.
- 25/10 : carte blanche ; 12 commits de `8e43227` à `88648a8` (lots 26 à 35 : caution acquise, parcours « app terminée », textes démo, audit et débug B1–B4, barème hôte, partenaire The Fork, annulation H−1, « compte fermé »), tous QA OK, 999 tests, poussés.
- 26/10 (7 h 25) : aucun commit ni fichier Moment modifié depuis 22 h 02 la veille.
- 26/10 (8 h 15) : lancement tâches 36 (audit + débug final sur `88648a8`) et 37 (argent annulation tardive lieu + polish NB lot 35) via ChatGPT, puis QA Testeur.
- 26/10 (8 h 30) : ChatGPT tip `97d9023` (81816cd débug 36 + lot 37) ; 3 B corrigés ; QA Testeur lancée.
- 26/10 (8 h 35) : QA Testeur OK sur `97d9023` (1038) ; lots 36+37 clos. NB mineurs notés ; 3 ouverts produit.
- 26/10 (reste de la journée) et nuit du 27/10 : aucun commit ni fichier Moment modifié après 8 h 35 ; tip `97d9023` poussé, branche à jour.
- 27/10 : aucun commit Moment ; tip `97d9023` inchangé ; résumé matinal = rappel des 3 ouverts produit.
- 28/10 (0 h 25) : création de HANDOFF.md ; résumé matinal resserré sur « tip inchangé → silence » ; Jev reste en shadow.
- 30/10 (~18 h 55) : Paolo tranche départ anticipé lieu = 20 € entiers ; lot 38 lancé via ChatGPT ; practices GrokBot.Rocks incorporées (skill, pas nouveaux agents).
- 30/10 (~19 h) : ChatGPT tip `2d48b53` lot 38 (1052) ; QA Testeur ; choix malaise lieu 20 € vs 13,10 à confirmer.
- 30/10 (~19 h) : Testeur BLOQUANT sur `2d48b53` (malaise lieu 20 €) ; attend tip 38b.
- 30/10 (~19 h) : ChatGPT tip `2d2fd8c` (38b malaise 0 €) ; re-QA Testeur.
- 30/10 (~19 h) : Testeur OK `2d2fd8c` ; lot 38 clos ; bots en pause.
