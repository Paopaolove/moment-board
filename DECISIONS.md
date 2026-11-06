# Registre des décisions Moment

Source de vérité unique. Toute décision de Paolo est notée ici, datée. En cas de conflit avec un brief, un bot ou du code : ce registre gagne.
Tenu par Grok Bot. Dev Moment, ChatGPT et Testeur Moment le lisent avant chaque tâche.

## Organisation
- 16/10 · V1 = branche feat/invitation-offer-lots (Paopaolove/chance). Ne bouge que sur décision de Paolo. Essais sur copies séparées.
- 16/10 · Équipe : Grok Bot coordonne · Dev Moment code · ChatGPT code certaines tâches (moins cher) · Testeur Moment valide avant chaque push (rapport avant/après).
- Process : brief → vérif règles → go de Paolo → code → QA → push. Pas de merge master, pas de force push, éviter 3bcb150.

## Règles figées
- Caution 20 € · partage 6,90 € Moment / 13,10 € hôte.
- 10 min pour confirmer · Joker 1/mois · Urgents H−90 à H+30.
- Option Femmes uniquement · Tables 1 à 3 places · Paris intramuros.
- L’hôte ne paie pas l’abonnement · Présence dès H−15.
- 16/10 · Textes des slides : PLUS figés (modifiables sur demande, tout changement signalé).

## Présence, absence, caution
- « Je suis arrivé » de H−15 jusqu’à la fin du moment, photo facultative, non obligatoire.
- Caution perdue seulement sur « Pas venu » signalé par l’hôte/partenaire (ou auto-déclaration d’absence par l’invité, perte immédiate), place vide, à partir de H. Refusé si l’invité a marqué sa présence. Tables normales : « Pas venu » strictement avant H+6 ; perte après 24 h sans contestation ou après la revue. Partenaires : même contestation sous 24 h (voir 17/10). Auto-déclaration d’absence : perte immédiate.
- Silence = caution rendue à H+6 (tables normales et partenaires, aligné 25/10 soir ; avant : partenaires = lendemain).
- Présence refusée après un « Pas venu ».
- 16/10 · Invité présent : caution rendue à H+30 (ou à la clôture par l’hôte), plus au marquage.

## Joker et départ (16/10)
- Joker : uniquement avant le début du moment.
- Bouton « Je quitte la table », sans justification.
- Départ avant 30 min sans motif : caution perdue (6,90 / 13,10).
- Motif malaise : caution rendue, rien compté, signalement confidentiel. Moment verse quand même 13,10 € à l’hôte : pour l’hôte, départ avec ou sans motif est identique.
- 2 malaises en 3 mois sans élément concret : accès au motif retiré, revue manuelle (caution du 2e quand même rendue).
- Départ après 30 min : libre, caution rendue.

## Règles complémentaires validées (16/10)
- Joker refusé si l’invité est déjà présent, même avant H.
- Pas de « Pas venu » contre un invité parti.
- Départ impossible après la fin du moment.
- Imprévu refusé : pas de perte de caution pour un invité présent ou parti. Imprévu traité à partir de H+6 : pas de perte (17/10).
- Poussé : 9f3e46b sur feat/invitation-offer-lots (121 tests).

## Clôture (17/10)
- Seul l’hôte peut clôturer le moment, à partir de H. L’invité peut signaler son départ (dont malaise) via « Je quitte la table ».

## Décisions du 17/10 (validées par Paolo)
- GO Signalement et revue + compteur hôte (Dev Moment, après clôture). (Le statut interne malaise est traité à part : voir la ligne suivante, GO du 17/10.)
- GO statut interne propre au malaise (caution rendue, Moment paie 13,10 € à l’hôte, vue hôte inchangée).
- Départ définitif — après « Je quitte la table », plus aucune annulation de cette réservation n’est possible, ni par l’invité ni par l’hôte (validé par Paolo).
- Bouton démo « Simuler sortie terminée » = clôture auto H+30 forcée, démo seulement (validé par Paolo).
- Deux clôtures distinctes. Annonce : sort du fil à H+30 ou dès que toutes les places sont prises ; tant qu’il reste une place, elle reste, même avec un accepté. Fin du moment : hôte à partir de H, sinon auto à H+30 (caution des présents, avis) ; ne change pas le fil. Seul ajout codé : un moment complet sort du fil.
- Menu démo (et clôture auto de démo) réservé au mode développement (__DEV__), absent en production.
- Signalement : possible seulement une fois le chat de la table ouvert (H−1 pour une table normale) — pas avant un échange. Membres = hôte + confirmés (partis compris, annulés exclus). Message fixe au signaleur « Merci pour ton signalement. Peux-tu nous en dire un peu plus ? ». Suspension = simple drapeau pour l’instant. Tous les malaises comptent pour le compteur hôte. Pas d’écran de file pour l’instant.
- Issue « abusif » : seulement si établi (la personne n’était pas là, ou reconnaît que c’était faux, ou plusieurs signalements sans aucun confirmé). Doute sans preuve = sans suite, jamais abusif. « Rien dans le chat » n’est pas un critère. Effet (fenêtre 3 mois) : 1er abusif établi = avertissement ; 2e = garde le droit de signaler, chaque signalement passe d’abord en revue ; pas de fermeture de compte pour ce seul motif. Répétition = au moins 2 autres signalements classés sans sanction.
- « Marquer présent et noter » (Profil) branché sur la vraie action de présence.
- Catégories de signalement (une seule + phrase libre) : Proposition ou geste déplacé ; Racisme ; Sexisme ; Insultes ou agressivité ; Menaces ; Ce n’était pas la personne ; Démarchage ; Autre. Le départ malaise n’est pas une catégorie.
- Notes sur 5, sans smileys. Avis négatif = 2 sur 5 ou moins (3 n’est pas négatif) (notation séparée du signalement).
- ~~Présence : seul l’hôte la marque~~ remplacé le 18/10 : confirmation croisée (voir 18/10). L’invité note après, si sa présence est établie.
- « Pas venu » (déclaré par l’hôte) est distinct du signalement. Un membre marqué « Pas venu » ne peut pas signaler. Notation et signalement séparés : aucun drapeau de revue lié aux avis ou au « Pas venu ».
- Après un départ malaise : ligne « Tu veux signaler ? » (Oui ouvre le formulaire, Non ferme). Rien de prérempli, rien d’envoyé sans confirmation. Départ et signalement restent séparés.
- Caution (tables normales, 17/10, remplace « silence = rendue le lendemain ») : la caution évite le no-show, la note n’a aucun effet sur l’argent. Les deux présents = rendue (à partir de H+30 ou de la clôture). Rien renseigné et pas de « Pas venu » avant H+6 = rendue à H+6. « Pas venu » avant H+6, place vide = perdue ; plus de « Pas venu » à partir de H+6. Imprévu traité après H+6 = pas de perte. Partenaires : même rendu à H+6 (25/10 soir ; avant = lendemain).
- Contestation d’un « Pas venu » : 24 h pour contester avec une phrase ; contesté = caution en attente de revue ; sans réponse à 24 h = caution perdue. Délai compté depuis la déclaration ; H+6 sans effet pendant le délai ou la revue ; deux issues (perdue / rendue). Côté hôte : « absence signalée · caution en attente », jamais la phrase.
- Hôte déclaré « Pas venu » : ne signale personne et ne peut déclarer aucun invité « Pas venu » ; les invités récupèrent leur caution.
- Signalement ouvert avant un « Pas venu » : maintenu, revue normale.
- Contestation acceptée (17/10, validé par Paolo) : absence effacée (ne compte plus, aucune sanction ni avertissement), l’invité peut de nouveau signaler et noter, caution rendue. L’hôte voit « absence non retenue » et ne touche pas les 13,10 €.
- Sanctions des 2e et 3e absences : attendent la fin des 24 h, ou la fin de la revue si l’absence est contestée. Aucune fermeture de compte tant que c’est en attente.
- Invité déjà déclaré « Pas venu », puis hôte déclaré absent : caution de l’invité rendue (le moment n’a pas eu lieu).
- Invité qui se déclare lui-même absent : caution perdue immédiatement, pas de contestation.
- Hôte déclaré « Pas venu » : il peut contester, 24 h, avec une phrase. Pendant ce délai et la revue, caution des invités en attente ; contestation rejetée ou absente = invités rendus (règle L60) ; acceptée = l’absence de l’hôte est effacée (validé par Paolo, 17/10).
- Partenaires : même contestation (24 h, une phrase, caution en attente de revue). L’auto-confirmation ne la supprime pas (17/10).
- Revue d’une contestation : 7 jours maximum ; sans décision à 7 jours = caution rendue (17/10).
- Dernier passage contestation (validé par Paolo, 17/10, aucun nouveau cas ensuite) :
  1. Hôte déclaré absent : on annule aussi la priorité baissée et la mention sur le profil de l’invité (en plus du compteur et de la fermeture). Précisé par le gel : l’absence de ce moment est retirée et les sanctions sont recalculées d’après les absences restantes.
  2. Revue non tranchée à 7 jours : rien n’est retenu ; absence non comptée, hôte comme invité ; invités « Pas venu » : caution rendue.
  3. Tant que l’absence de l’hôte est en attente, les 24 h de l’invité « Pas venu » sont suspendues.
  4. Invité « Pas venu » ayant déclaré l’hôte absent : la décision sur l’hôte tranche son cas (hôte absent = caution rendue ; hôte présent = caution perdue).
  5. Contestation de l’hôte acceptée : il était là, il garde le droit de déclarer un « Pas venu » jusqu’à H+6.
  6. Partenaire : « Je suis arrivé » après un « Pas venu » vaut contestation. Lieu déclaré absent : même règle que l’hôte.
- Gel de la contestation (validé par Paolo, 17/10, 19 h 20), version la plus simple :
  1. Toute déclaration d’absence (invité, hôte, lieu partenaire) : seulement de H à H+6.
  2. Une seule déclaration d’absence par personne et par moment (un acquitté ne peut pas être redéclaré).
  3. La contestation reste possible pendant la suspension des 24 h.
  4. Les sanctions sont recalculées d’après le nombre d’absences restantes.
  5. Plus aucun nouveau cas sur la contestation.
- Hôte déclaré « Pas venu » : déclarable jusqu’à H+6, pas après (validé par Paolo, 17/10).
- Invité déjà « Pas venu », pendant ses 24 h : il peut déclarer l’hôte absent ; cela vaut contestation et passe en revue, caution pas rendue d’office. Revue retient que l’hôte n’était pas là = caution rendue ; sinon perdue (17/10).
- Absence définitive : message à l’invité « Ton absence est retenue. La caution est perdue. » (17/10).
- Contestation acceptée : l’hôte ne peut plus déclarer le même invité « Pas venu » ; elle vaut présence, l’invité peut noter (validé par Paolo, 17/10).
- Hôte déclaré absent : caution de l’invité rendue et absence (« Pas venu ») effacée, même si la caution était déjà définitivement perdue. Sauf auto-déclaration d’absence par l’invité : caution perdue (17/10).
- Joker toujours invisible pour l’hôte, avant comme après H+6 : mêmes libellés qu’un rendu ordinaire, aucun message « Joker » côté hôte (17/10).
- Côté hôte, la ligne « X · caution rendue » ne s’affiche qu’à partir de H+6, sauf si l’hôte est déclaré « Pas venu ». Avant, aucune ligne : le joker reste invisible (validé par Paolo, 17/10).
- 5 choix du Testeur gardés : compteur warnings partagé ; revue préalable décidée à la création ; 3 mois depuis la clôture de l’abusif ; motifs déclarés par Moment ; au moins un confirmé.
- Suppression de « Pas pour draguer » du profil.
- moment-gpt-pro : ni le crédit ni le brief en 3 points ne sont importés (clos).

## Signalement et revue (16/10)
- Tout membre (invité ou hôte) peut signaler, pendant ou après le moment.
- Revue : signalement → contact signaleur → contact concerné (« Est-ce que tout s’est bien passé ? », sans révéler le signaleur) → décision (sans suite / avertissement / suspension / signalement abusif).
- Compteur côté hôte : 2 départs pour malaise en 3 mois à ses tables → revue de l’hôte (arrive avec la tâche Signalement).

## En attente de décision
- (aucune décision en attente de l’ancienne liste : toutes tranchées le 17/10)

## Avant mise en production (non bloquant tant qu’il n’y a pas de build store)
- Mentions « (démo) » / « (mock) » encore visibles en prod (ex. « Continuer avec Apple (démo) », « Formule activée (démo) », « Caution remboursée (mock). »).
- Candidatures partenaires : validation seulement dans le menu démo ; il faudra une interface d’administration.
- Revue d’une contestation de « Pas venu » : déclenchable nulle part pour l’instant (outil de revue à prévoir).
- Minuteries H+6 et 24 h de contestation calculées sur l’horloge du téléphone : à passer côté serveur.
- Clôture automatique horodatée par le serveur.

## 18/10 · Présence : confirmation croisée (validé par Paolo)
- Trois mécaniques séparées : présence (seule à toucher la caution), note après le moment (aucun effet sur l’argent ni sur le signalement), signalement (bouton de sécurité, 8 catégories + phrase, aucun effet sur caution ni note).
- Chacun peut dire « je suis présent » et confirmer la présence de l’autre : l’invité pour lui et pour l’hôte, l’hôte pour lui et pour chaque invité. Fenêtre inchangée (H−15 à H+6).
- Une seule confirmation (la sienne ou celle de l’autre) suffit : présence établie, caution rendue, note possible.
- Désaccord (« présent » d’un côté, « Pas venu » de l’autre) : contestation, même procédure (24 h, revue 7 jours max). Remplace « Pas venu refusé si l’invité a marqué sa présence ».
- Silence des deux côtés : caution rendue à H+6 (inchangé).
- À la fin du moment, notification (pas SMS) à qui n’a rien indiqué : « Alors, comment ça s’est passé ? Es-tu bien présent ? ».

- Validé par Paolo (18/10, commit 4383820) : présence confirmable jusqu’à H+6 même après clôture par l’hôte. Textes « Contestation ouverte », « s’est dit présent », fenêtre « de 15 min avant à 6 h après ».
- Caution déjà rendue = acquise : un désaccord ultérieur part en revue pour la sanction seulement, on ne reprend jamais l’argent (18/10).
- Partenaire : fenêtre présence/absence H+6 déjà dans 4383820. 25/10 soir : caution silence aussi à H+6 (plus le lendemain). Pas de badge Fiable dans ce lot.

## 25/10 · Carte blanche (Paolo)
- Paolo donne carte blanche à Grok Bot pour terminer l’application, avec rapport d’avancement. Enchaînement : lots → audit → débug.
- Tous les points en suspens doivent être résolus pour tester l’app comme terminée ; vigilance sur la cohérence et la logique.
- Le contrôle Expo Go sur le lot « caution rendue = acquise » est levé : le bot ChatGPT finit tests, commit et push sur feat/invitation-offer-lots.

## 25/10 · Points tranchés sous carte blanche (cohérence V1 testable)

Objectif Paolo : pouvoir tester l’app comme terminée, sans trou logique.

### Fenêtres et bornes
- H+6 **inclus** pour déclarer une absence (« de H à H+6 »). Après H+6 : plus aucune nouvelle déclaration.
- Un moment qui commence avant minuit et déborde : la fenêtre H+6 se calcule depuis l’heure de début H, sans coupure à minuit.
- Départ « 30 minutes » : le compteur part de **H** (début du moment). À exactement 30 min : traité comme « après 30 min » (caution rendue si pas d’autre motif de perte).

### Contestation et revue
- Qui déclare l’hôte absent : tout **invité confirmé** du moment (y compris déjà « Pas venu », auquel cas cela vaut aussi sa contestation). Personne d’autre.
- Début des **7 jours** de revue : à l’instant où la contestation est déposée (phrase envoyée).
- Reprise des **24 h** après gel (absence hôte en attente) : **temps restant** au moment du gel, pas un nouveau délai de 24 h.
- Après contestation **acceptée** de l’hôte : l’hôte peut de nouveau déclarer « Pas venu » seulement si on est encore dans H→H+6 ; sinon la fenêtre est close.
- Outil de **revue des contestations** : écran / actions accessibles en démo (__DEV__ et menu démo) pour trancher perdue / rendue, afin de tester le parcours de bout en bout sans serveur d’admin.

### Sanctions d’absence (barème)
Sur **3 mois** glissants, absences **retenues** seulement :
- 1re : pas de sanction au-delà de la perte de caution du moment ;
- 2e : priorité baissée ;
- 3e : fermeture du compte (après revue manuelle courte si contestation encore ouverte sur l’une d’elles : aucune fermeture tant que c’est en attente).

### Signalement
- Délai après le moment : signalement possible jusqu’à **7 jours** après la fin du moment (clôture ou H+30 auto). Au-delà : fermé.

### Présence / caution (rappel aligné 18/10)
- Une seule confirmation suffit (« les deux présents » n’est plus exigé).
- Caution déjà rendue = acquise (lot code en cours).

### Hors V1 Moment (clos pour ce chantier)
- Crédit moment-gpt-pro (tâche 6) : **hors Moment V1**, pas bloquant pour tester Chance/Moment.
- Minuteries et clôture **côté serveur** : restent avant build store ; en démo, horloge appareil + outil de revue + simulations démo existantes doivent suffire pour un parcours complet cohérent.
- Admin candidatures partenaires : validation via menu démo suffisante pour tester ; vraie admin = avant store.
- Mentions « (démo) » / « (mock) » : à retirer ou masquer hors __DEV__ pour que le parcours de test ressemble à une app finie.
- Table normale : pas de désistement à partir de H (bouton masqué) ; comportement confirmé en QA 25/10 sur 782d36c.
- Barème d’absences sur 3 mois : **invités** (1 / 2 / 3). Hôte « Pas venu » : barème figé distinct (1er avertissement, 2e compte fermé) — rétabli 25/10 soir. Revue malaise hôte (2 en 3 mois) inchangée.

## 25/10 · Débug audit (78284a1)
- completed ne repasse jamais en closed après une absence post-clôture.
- Annulation hôte refusée dès H (inclus) ou si un invité est présent/parti.
- Prod : invité peut déclarer « L’hôte n’est pas venu » et « Je ne suis pas venu » (H→H+6).
- Barème hôte « Pas venu » : retiré dans 78284a1 (L160), **rétabli le soir du 25/10** (voir section suivante).
- Ouvert à acter plus tard : règle « publication jamais honorée » (démo) au registre. Badge Fiable : hors de ce lot.

## 25/10 soir · Deux corrections (Paolo)
### 1. Hôte déclaré « Pas venu » — barème figé rétabli
- 1re absence d’hôte **retenue** : avertissement.
- 2e : compte fermé.
- Les invités récupèrent leur caution (inchangé).
- Barème **invité** inchangé : 2e priorité baissée, 3e fermeture, fenêtre 3 mois.
- Remplace L160 / la note « pas de barème hôte » du débug 78284a1.

### 2. Partenaire — même horloge que la table
- Caution rendue à **H+6** s’il n’y a rien (silence), plus « le lendemain ».
- Caution silence partenaire à H+6 : fait dans `4bc4393`.
- Soirée lieu « Je suis arrivé / Pas venu » : **remplacée** le même soir par Partenaire The Fork (section suivante).
- Pas de badge Fiable dans ce lot.

## 25/10 soir · Partenaire calé The Fork (version simple)
Remplace le soir partenaire « Je suis arrivé / Pas venu » côté lieu par une seule action type The Fork. **Table normale inchangée.**

### Soirée lieu
- À **H+30** : notification au lieu avec la **liste des prénoms confirmés**.
- Seule action du soir : « **Table complète** », ou **décocher** celui qui n’est pas là.
- Rien coché à **H+6** : cautions rendues (silence, même horloge que la table — cohérent avec la correction H+6 du même soir).
- Un **self-check** invité seul **ne rend pas** l’argent.

### Invité décoché (marqué absent par le lieu)
- Message : « Le lieu t’a marqué absent ».
- **24 h** pour dire « je suis venu », avec une phrase → contestation.
- Contesté : revue, caution en attente.
- Pas de réponse, ou revue **retenue** : **20 € entiers au lieu** (pas le split 6,90 / 13,10 des tables normales).
- Revue non retenue / contestation acceptée : caution rendue, absence non comptée.

### Sanctions
- **4 absences retenues en 12 mois** (sur moments partenaire) : compte fermé (barème partenaire distinct).
- Barème invité table normale inchangé (2e priorité, 3e fermeture, 3 mois).
- Barème hôte table normale inchangé (1 avertissement / 2 fermeture).
- Pas de badge Fiable dans ce lot.

### Hors scope ce lot
- Badge Fiable, admin candidatures réelle, timers serveur, table normale.

## 25/10 soir · Annulation invité : H−1 (plus 3 h)
- Avant **H−1** : caution **rendue**.
- Après **H−1**, ou absent : caution **perdue**.
- **Joker** : inchangé — 1 fois par mois, **même dans l’heure** (avant H, refusé si déjà présent).
- Remplace la règle « au moins 3 heures avant ».
- Table normale et textes / pricing / clock / onboarding / ConfirmSlot à aligner. Partenaire : même borne d’annulation invité sauf si The Fork (33) définit autrement le soir lieu.

## 25/10 soir · Trois points produit (Paolo)
### 1. Auto-déclaration d’absence sur un moment lieu
- Invité qui se déclare absent sur un **partenaire** : compte dans le **barème partenaire** (4 absences retenues en 12 mois → compte fermé).
- **Pas** le barème table normale (2e priorité / 3e fermeture / 3 mois).
- Caution : perte immédiate (règle auto-déclaration inchangée) ; pour un lieu, l’argent suit la logique partenaire (20 € au lieu si retenu / silence après 24 h — aligné The Fork).

### 2. ConfirmSlot partenaire
- Sur un moment **lieu** : texte « trop tard ou absent » = **20 € entiers au lieu**.
- Plus de split **6,90 / 13,10** sur ConfirmSlot partenaire.
- **Table normale inchangée** (6,90 Moment / 13,10 hôte).

### 3. Libellés
- UI : **« compte fermé »** partout.
- Plus de **« suspendu »**, plus de **« ban »** visibles à l’utilisateur (y compris démo).
- Identifiants code internes (`banned`, etc.) OK s’ils ne fuient pas dans l’UI.

## 26/10 · Ouvert produit (audit 36)
- ~~**Départ anticipé sur un lieu**~~ → tranché 30/10.
- ~~Bandeau Caution / compteur x/4~~ → tranché 31/10 (section suivante).

## 30/10 · Départ anticipé lieu = 20 € (Paolo)
- Sur un moment **lieu**, départ anticipé **sans malaise**, **avant 30 min** : **20 € entiers au lieu**.
- Plus de split **6,90 / 13,10** pour ce cas lieu.
- Aligné sur absence retenue lieu, annulation tardive lieu, ConfirmSlot partenaire.
- **Table normale inchangée** (départ avant 30 min sans motif = 6,90 Moment / 13,10 hôte).
- **Malaise** : caution **invité** rendue, comme partout.
- **Malaise sur un lieu** (30/10) : **0 € au lieu** (ni 20 ni 13,10). Motif invisible : le lieu voit « parti », pas « malaise ».

## 31/10 · Bandeau Caution + compteur lieu (Paolo)
### 1. Bandeau « Caution perdue »
- **Pas à vie** : aucun bandeau permanent sur le Profil.
- Visible **sur le moment** concerné et **dans l’historique** de ce moment.
- Pas d’autre surface permanente.

### 2. Compteur absences lieu
- Affiché **pour l’intéressé seul** : libellé **« N sur 4 »** (absences **retenues**, fenêtre **12 mois**).
- ~~À **4** retenues → **compte fermé**~~ → remplacé 01/11 (section suivante).
- **Invisible** pour hôte, autres invités, lieu.

## 31/10 · Audit lot 39 (Paolo)
1. Note auto fil **table normale** : **neutre** (comme le lieu) — absence + argent, jamais le barème / compte fermé visibles à l’hôte.
2. Ligne **« Caution perdue »** dans **Moments passés** (Profil) : **oui** — sur le moment et dans son historique ; pas de bandeau permanent.
3. Supprimer **`guestNoShowCount`** et **`partnerNoShowCount`** (doublons) ; sources = logs / strikes + recalcul fenêtre.


## 01/11 · Ban 1 mois puis fermeture (Paolo) — remplace fermeture immédiate à 4
Barème **absences lieu** (partenaires, retenues, 12 mois), invité seul :
1. Affichage **« N sur 4 »** inchangé (invisible aux autres).
2. À **4** retenues → **compte fermé temporairement pendant un mois à cause des absences**, **partout dans Moment** (pas seulement les lieux).
3. Libellé UI exact (Paolo) : **« compte fermé temporairement pendant un mois à cause des absences »** + **date de fin** (pas « ban » / « suspendu » ; ne pas raccourcir à « fermeture temporaire » seule).
4. Pendant cette période : tout message / action bloquée doit **marquer** ce libellé (pas seulement « expiré »).
5. Après la fin de ce mois : le compteur affiché passe à **« 1 sur 1 »** (plus « N sur 4 ») ; **une** absence lieu retenue → **compte fermé** définitif.
6. Remplace la règle « 4 = compte fermé immédiat » (31/10 / lots 35–39).

## 01/11 · Lot 41 acté (Paolo)
Tip `d625af7`, QA OK. Validé :
1. Absence retenue pendant le mois temp → journal seulement ; pas de fermeture définitive ni prolongation.
2. Après le mois → compteur **« 1 sur 1 »** ; une absence lieu retenue → compte fermé définitif (même si le compteur 12 mois est retombé ; fermeture temp une seule fois).
3. Date de fin = +1 mois calendaire depuis la 4e retenue.
4. `joinOuting` bloqué aussi pour compte fermé **définitif** (aligné confirmSlot).
5. **Libellé papier / UI (mots exacts Paolo, 01/11 vocal)** : « compte fermé temporairement pendant un mois à cause des absences ». Pendant la fermeture temporaire, ne pas essuyer / remplacer par un message générique (« expiré ») : **marquer** ce libellé.
6. **Lot 42 à coder** :
   - Toast « Absence retenue » (4e) : mentionner aussi « compte fermé temporairement pendant un mois à cause des absences » (+ date).
   - Après le mois de fermeture temp : face au compteur, afficher **« 1 sur 1 »** (pas « 1 sur 4 ») jusqu’à la fermeture définitive.

## 01/11 · Message fermeture définitive (Paolo, vocal) — **validé tel quel**, lot 42
« Ton compte est fermé définitivement.

Après quatre absences, on t’avait laissé un mois pour reprendre — compte fermé temporairement à cause des absences. Tu as de nouveau été absent. Les absences sont un point critique de Moment : sans confiance sur la venue, ça ne tient pas. C’est donc terminé, sans limite de temps. »

## 06/11 · Look V1 = look Moment Pro (Paolo) — esthétique seulement
- Porter le look de moment-gpt-pro sur V1 (`feat/invitation-offer-lots`, départ `1a954c6`). **Ne pas merger** le proto : jetons / typo / rythme / icônes seulement.
- Palette : fond blanc `#FFFFFF`, surfaces `#F7F7F5`, encre `#111111`, CTA `#1F2937`. Inter Tight pour l’UI ; Fraunces pour le mot-symbole seulement.
- Cartes aérées, icônes dessinées, cibles 44 px, beaucoup d’air.
- Interdit : abricot, papier `#F7F1EA`, vert jaguar `#1B4D3E` / `#143D32`.
- Slides, montants, délais, libellés : **inchangés**. Aucune règle métier.
- Lot 43 + 43b poussés `5bee1de` (06/11), QA OK.

## 06/11 · Signets (Paolo) — lot 44
- Un **signet** sur la **carte** d’un moment.
- Une **liste** dans le **Profil** (soi seul).
- Ce n’est **pas** une demande : poser ou retirer un signet ne crée aucune demande, ne réserve aucune place.
- **Personne n’est prévenu** (ni hôte, ni autres invités, ni lieu).
- **Passé ou complet** : le moment **sort de la liste**.
  - **Complet** = plus de place (`full` / plus de `spotsLeft`), même logique que le fil.
  - **Passé** = moment révolu (heure de début dépassée, ou terminé / `completed`).
- Pas de « X personnes regardent ». Pas de « populaire ». Aucun compteur ni signal social autour des signets.
- Métier inchangé : caution, barèmes, délais, présence, libellés d’écran existants.

