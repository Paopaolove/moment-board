# Mémoire collective Moment

Source de vérité des décisions produit de Moment, l’app Expo / React Native de Paolo (Paolove) pour des invitations IRL à Paris (resto, bar, culture, sport). Ce n’est pas une appli de rencontres.

Ce dépôt est public pour que SuperGrok et tous les bots puissent le lire sans coller un brief.

## Comment lire

1. Commence par [`HANDOFF.md`](HANDOFF.md) : tip git actuel, objectif, décisions figées, sujets ouverts.
2. Règles détaillées : [`DECISIONS.md`](DECISIONS.md). **Ce fichier gagne** en cas de conflit avec un souvenir, un proto GPT ou un ancien brief.
3. Résumé d’une page : [`REGLES-1-page.md`](REGLES-1-page.md)
4. Suivi des lots : [`TABLEAU.md`](TABLEAU.md)
5. Contexte, rôles et journal : [`PROJET.md`](PROJET.md)

## Règles pour un bot qui lit ce dépôt

- Travaille en français, de façon factuelle.
- N’invente aucune règle. Ne rouvre pas une décision déjà tranchée.
- Ne change pas un montant, un partage, un délai ou un libellé d’écran sans demande explicite de Paolo.
- En cas de doute entre table normale et lieu partenaire (partage 6,90 / 13,10 € contre 20 € au lieu, malaise contre départ simple), demande confirmation avant d’écrire du code.
- Le code à jour est sur la branche `feat/invitation-offer-lots` du dépôt `Paopaolove/chance`. Les prototypes dans `Paopaolove/moment-gpt` se sont arrêtés vers le 16/10/2026 : les décisions prises après cette date n’y sont pas portées.
- Pas de paiement réel, pas de Stripe live, pas d’EAS, pas de store. Pas de force-push, pas de merge de `master`.

## Maintenance

Grok Bot met à jour ces fichiers à chaque décision ou lot clos, puis pousse ici.

Dernière publication : 6 novembre 2026, Europe/Paris (tip V1 `5bee1de`, lots 43 + 43b clos).
