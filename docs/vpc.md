# Value Proposition Canvas — Livrable S2

Version visuelle : [vpc.pdf](assets/vpc.pdf) · [vpc.png](assets/vpc.png)

Persona : **Ndèye, chargée de recouvrement, NSIA Vie Assurances** (voir la [carte d'empathie](../carte-empathie.md)).

## PROFIL CLIENT

### Jobs to be done
- Repérer les assurés en retard de cotisation Wave / Orange Money.
- Relancer chaque retardataire au bon moment, avec le bon message.
- Enregistrer chaque versement sur le bon numéro de police.
- Rendre compte à la direction : montant recouvré, arriérés restants.
- Préparer la création d'un service de recouvrement dédié.

### Pains
- **P1** Pas de vue d'ensemble des retards (qui, depuis quand, combien).
- **P2** Rapprochement manuel paiement ↔ contrat : lent et source d'erreurs.
- **P3** Relances sans historique : on oublie ce que le client a promis.
- **P4** Tout repose sur une seule personne.
- **P5** Aucun indicateur pour prouver les résultats.

### Gains
- **G1** Savoir chaque matin qui relancer en premier.
- **G2** Moins de temps de saisie, zéro relance inutile.
- **G3** Plus de contrats maintenus, moins d'arriérés.
- **G4** Des chiffres clairs pour défendre le futur service.

## PROPOSITION DE VALEUR — RecouvIA

### Produits & Services (MVP V0)
Un tableau de bord web de suivi du recouvrement. La chargée importe la liste des contrats et les relevés Wave / Orange Money ; l'outil rattache les paiements aux numéros de police, classe les retards par priorité, propose un message de relance rédigé par IA et garde l'historique de chaque échange.

### Pain Relievers
- **PR1** → P1 : liste « À relancer aujourd'hui » triée par score (jours de retard × montant dû × risque de déchéance).
- **PR2** → P2 : import des relevés Wave/OM et rapprochement automatique par numéro de police, puis téléphone ; les cas douteux sont signalés pour vérification.
- **PR3** → P3 : fiche client avec journal des relances et promesses de paiement, rappel à la date promise.
- **PR4** → P4 : messages de relance pré-rédigés par un agent IA (français / wolof), validés en un clic ; le travail peut être réparti entre plusieurs agents plus tard.
- **PR5** → P5 : indicateurs automatiques (recouvré du mois, arriérés, taux de maintien, promesses tenues).

### Gain Creators
- **GC1** → G1 : vue matinale en moins de 5 minutes au lieu d'un tri manuel.
- **GC2** → G2 : le versement saisi une seule fois, contrôle anti-doublon.
- **GC3** → G3 : relance plus tôt et plus personnalisée, donc plus de clients qui reprennent leurs versements.
- **GC4** → G4 : rapport mensuel exportable pour la direction.

## Vérification du FIT

| Pain | Pain Reliever | Couvert ? |
|---|---|---|
| P1 Pas de vue d'ensemble | PR1 Liste priorisée | Oui |
| P2 Rapprochement manuel | PR2 Import + rapprochement | Oui |
| P3 Pas d'historique | PR3 Journal des relances | Oui |
| P4 Une seule personne | PR4 Messages IA + outil partageable | Partiel : l'outil soulage, le recrutement reste une décision de la direction |
| P5 Pas d'indicateurs | PR5 Indicateurs automatiques | Oui |

Aucun Pain Reliever orphelin : chacun répond à un Pain identifié.
