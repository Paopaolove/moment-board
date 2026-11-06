# Tableau des tâches Moment

Statuts : À faire · En cours · Bloqué · À valider (Paolo) · Fait
Équipe (depuis le 21/10, fin du mode économie) : Grok Bot (coordination, DECISIONS.md, PROJET.md) · ChatGPT (tout le code Moment) · Testeur Moment (QA complète) · Dev Moment (à l'arrêt).

| # | Tâche | Responsable | Statut | Note |
|---|---|---|---|---|
| 1 | Brief des 3 points issus de la version GPT (Sport/Culture/Autre ton éditorial, texte caution plus clair, lignes d'ambiance sur les cartes) | Grok Bot | Fait | Abandonné : Paolo 17/10, ne pas importer le brief ni le crédit de moment-gpt dans Moment |
| 2 | Joker utilisable après le début du moment ? | Paolo | Fait | Tranché le 16/10 : joker uniquement avant le début |
| 3 | Phrase « draguer » dans EditProfileScreen | Dev Moment | Fait | Phrase retirée, commit 3a49557 (17/10) |
| 4 | Procédure de contestation d'un « Pas venu » (invité, hôte, partenaire, revue 7 jours) | Dev Moment | Fait | Tranchée et codée le 17/10 (89a2182 à b376288), gelée par Paolo à 19 h 20 (082463e), poussé |
| 5 | moment-gpt-pro : règle absence/caution corrigée | ChatGPT | Fait | Commits 2da428a, 566c6fa, 746f6b8 |
| 6 | moment-gpt-pro : crédit défini par hypothèse | — | Fait | Clos 25/10 : hors Moment V1 |
| 7 | Rangement des signets X (reste avant le 13/07/2026 et mi-sept.–oct.) | Grok Bot | En attente | 45 rangés sur ~130+ |
| 8 | Tunnel pour voir moment-gpt-pro sur iPhone | Grok Bot | À faire | Sur demande |
| 9 | V1 : « Je quitte la table », joker avant H, caution des présents à H+30, départ malaise indiscernable pour l'hôte | Dev Moment + Testeur | Fait | Poussé 9f3e46b sur feat/invitation-offer-lots (16/10, 121 tests) |
| 10 | Clôture du moment (COMPLETE_OUTING) : hôte seul à partir de H, auto H+30 inchangée | Dev Moment | Fait | Tranché le 17/10, commit 4b49d2a |
| 11 | Statut interne propre au malaise (returned_discomfort_leave), vue hôte inchangée | Dev Moment | Fait | GO du 17/10, commit c888e16 |
| 12 | Signalement et revue (3 étapes) + compteur hôte (2 malaises en 3 mois) | Dev Moment | Fait | Commits d2356b7, 600ea8c, 23e4ebb, poussés |
| 13 | moment-gpt-pro : passages 1 à 4 (cahier des charges, domaine testé, interface refaite) | ChatGPT | Fait | Commits 21de78d à 7c71cde (16/10) |
| 14 | Démo « Simuler sortie terminée » = clôture auto H+30 forcée | Dev Moment | Fait | Commit 4fa7859 (17/10) |
| 15 | Un moment complet sort du fil d'annonces | Dev Moment | Fait | Commits 5cc6015, 5fc84c8 (17/10) |
| 16 | Menu et fonctions démo réservés à __DEV__ | Dev Moment | Fait | Commits 5f0e18f, 782aec8, 44eefe0 (17/10), poussés |
| 17 | « Marquer présent et noter » : hôte seul, invité par invité, avis si présent | Dev Moment | Fait | Commits 31381fe, ad351b6, poussés |
| 18 | Catégories signalement (8) + ouverture avec le chat + effet abus 3 mois | Dev Moment | Fait | Commit 23e4ebb, aligné DECISIONS.md 17/10, poussé |

| 19 | Caution tables normales rendue d'office à H+6, libellés de refus en français | Dev Moment | Fait | Commits 5adaef0, d064519, 6917976, 7106590 (17/10), poussés |
| 20 | Signalement : un invité « Pas venu » ne signale pas, « Tu veux signaler ? » après un départ malaise, confidentialité côté hôte | Dev Moment | Fait | Commits 5f27dbf, 64b2093, d1efc9a (17/10), poussés |
| 21 | Résumé des règles et points à trancher, puis REGLES-1-page.md | Grok Bot + ChatGPT | Fait | 17/10 18 h 42 et 19 h 23 |
| 22 | Vérification : npm run verify, hook pre-push, carte des écrans docs/FEATURE-MAP.md | ChatGPT | Fait | Commits b43ab5e, db409ea, 879a0de (17/10 21 h 53), poussés |
| 23 | Résumé de la vidéo de Lauren Tan (vérifier avec des agents) | Grok Bot | Fait | 17/10 21 h 46 |
| 25 | Présence : confirmation croisée (invité et hôte, H−15 à H+6 même après clôture, désaccord = contestation, textes « Contestation ouverte. » / « S’est dit présent. »), notification de fin à qui n’a rien indiqué | non vérifié | Fait | Validé par Paolo le 18/10, commit 4383820, poussé |
| 26 | Caution déjà rendue = acquise (+ 3 correctifs QA) | ChatGPT + Testeur | Fait | 8e43227 + 782d36c. QA Testeur OK sur b10a8c6 |
| 24 | Avant store : minuteries/clôture serveur, admin candidatures partenaires | — | À faire | Hors parcours démo testable ; reporté avant build store |
| 27 | Parcours testable « app terminée » (8 points 25/10) | ChatGPT + Testeur | Fait | b10a8c6, QA OK. Suite non bloquante → Lot C |
| 28 | Lot C : libellés démo hors __DEV__ + levée auto priorité/mention hors 3 mois | ChatGPT + Testeur | Fait | 3fb9efa, QA OK |
| 29 | Micro D : masquer « Mode démo local » profil hors __DEV__ | ChatGPT | Fait | 6448264 |
| 30 | Audit + débug B1–B4 | ChatGPT + Testeur | Fait | 78284a1, QA OK |
| 31 | Lot E polish : refresh UI à H/H+6 + paywall hors __DEV__ | ChatGPT + Testeur | Fait | 7aafa27, QA OK |

| 32 | Corrections : barème hôte figé (1 avert. / 2 fermeture) + partenaire caution H+6 | ChatGPT + Testeur | Fait | 4bc4393, QA OK (959). NB : libellé « suspendu »/« ban » ; bandeau double avert. ; self-check partenaire → 33 |

| 33 | Partenaire The Fork (H+30 liste, décocher, 20 € lieu, H+6 silence, 4/12 mois) | ChatGPT + Testeur | Fait | e90edb9 dans 69c83d7 ; QA OK |

| 34 | Annulation invité : borne H−1 (plus 3 h) ; joker inchangé même dans l’heure | ChatGPT + Testeur | Fait | efd2d1e, QA OK (985). NB commentaires pricing/mockOutings |

| 35 | Auto-décl. partenaire 4/12 + ConfirmSlot 20 € lieu + libellés « compte fermé » | ChatGPT + Testeur | Fait | 88648a8, QA OK (999). NB : argent annulation tardive lieu = textes ; toast double ; shareWho mort ; Suspension tableReports |
| 36 | Audit complet puis débug final sur 88648a8 (demande Paolo 25/10) | Grok Bot + ChatGPT + Testeur | Fait | 81816cd (3 B). QA OK sur **97d9023** (1038). Audit : /workspace/chance-audit-88648a8.md |
| 37 | Argent annulation tardive lieu (20 €) + polish toast/shareWho/Suspension | ChatGPT + Testeur | Fait | **97d9023**, QA OK |
| 38 | Départ anticipé lieu 20 € ; malaise lieu 0 € + « parti » (38b) | ChatGPT + Testeur | Fait | **`2d2fd8c`**, QA OK (1055) |
| 39 | Bandeau Caution (pas à vie) + compteur lieu « N sur 4 » privé | ChatGPT + Testeur | Fait | **`24a1da1`**, QA OK (1069) |
| 40 | Audit 39 : note neutre + Caution Moments passés + drop counts | ChatGPT + Testeur | Fait | **`08f6f0b`**, QA OK (1087) |
| 41 | À 4 absences lieu → compte fermé temporairement pendant un mois à cause des absences (partout) + date ; 1 absence après → fermeture définitive | ChatGPT + Testeur | Fait | **`d625af7`**, QA OK (1111). Libellé exact Paolo ; join bloqué si fermé définitif acté |
| 42 | Toast 4e + fermeture temp ; compteur **« 1 sur 1 »** après mois ; message fermeture définitive (texte Paolo validé) | ChatGPT + Testeur | Fait | **`1a954c6`**, QA OK (1126) |
| 43 | Look Moment Pro sur V1 (esthétique seule : blanc / #F7F7F5 / #111111 / CTA #1F2937, Inter Tight, Fraunces mot-symbole, cibles 44 px) | ChatGPT + Testeur | Fait | **`5bee1de`** (parent `fed184c`). QA OK (1126). |

Dernière mise à jour : 06/11/2026 ~11 h 20 Europe/Paris (lot 43 clos `5bee1de`, QA OK)
