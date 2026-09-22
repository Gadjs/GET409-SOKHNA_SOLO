# GET409-SOKHNA_SOLO — RecouvIA

Projet de recouvrement pour **NSIA Vie Assurances** — GET 409 Atelier IA, Master 1, Swiss UMEF University (Campus de Dakar), 2025-2026.

## HMW définitif

> **« Comment pourrions-nous permettre à la chargée de recouvrement de NSIA Vie Assurances de repérer chaque jour les assurés en retard de cotisation Wave ou Orange Money et de suivre leurs relances, afin de réduire les arriérés et de ramener ces clients à poursuivre leurs versements ? »**

## Équipe SOKHNA_SOLO

| Membre | Rôles | Contact |
|---|---|---|
| Sokhna GADIAGA | Chef de Produit · Master Prompt Engineer · Dev UI · Responsable Impact | gadiagasokhnaawa28@gmail.com |

## Le défi

**Secteur :** inclusion financière — assurance vie et paiement mobile (Wave, Orange Money).

**Problème :** les assurés qui cotisent par Wave ou Orange Money accumulent des retards, parce que le suivi des paiements et des relances repose sur une seule chargée de recouvrement travaillant avec des fichiers manuels. Les arriérés grossissent et des contrats tombent en déchéance.

**Persona :** Ndèye, chargée de recouvrement chez NSIA Vie Assurances à Dakar.

**Insight clé :** le problème n'est ni la volonté de payer des clients ni l'effort de la chargée : c'est le manque de visibilité sur qui relancer, quand, et ce qui a été promis.

## La solution envisagée — MVP V0

**RecouvIA**, un tableau de bord de suivi du recouvrement :

- import des contrats et des relevés Wave / Orange Money ;
- rattachement automatique de chaque paiement à son numéro de police ;
- liste « À relancer aujourd'hui » classée par priorité ;
- messages de relance proposés par un agent IA (français / wolof), validés par la chargée ;
- historique des relances et des promesses de paiement ;
- indicateurs mensuels : recouvré, arriérés, taux de maintien des contrats.

## Livrables

```
GET409-SOKHNA_SOLO/
├── README.md
├── carte-empathie.md        (S1)
├── guide-interview.md       (S1)
├── hmw.md                   (S1)
├── journal-prompts.md       (S1)
├── fiche-equipe.md          (S1)
└── docs/                    (S2)
    ├── chapeaux-bono.md
    ├── hmw-definitif.md
    ├── journal-prompts-s2.md
    ├── pitch-hmw.md
    ├── vpc.md
    └── assets/              (PDF et images)
```

### Séance 1 — Empathize → Define
| Livrable | Fichier |
|---|---|
| Fiche d'équipe | [fiche-equipe.md](fiche-equipe.md) · [PDF](docs/assets/fiche-equipe.pdf) |
| Guide et notes d'interview | [guide-interview.md](guide-interview.md) |
| Carte d'empathie | [carte-empathie.md](carte-empathie.md) · [PDF](docs/assets/carte-empathie.pdf) |
| Énoncés HMW (brouillon) | [hmw.md](hmw.md) |
| Journal de prompts S1 | [journal-prompts.md](journal-prompts.md) |

### Séance 2 — Ideate + Prompt Engineering
| Livrable | Fichier |
|---|---|
| Idéation (6 chapeaux de Bono) | [docs/chapeaux-bono.md](docs/chapeaux-bono.md) |
| Value Proposition Canvas | [docs/vpc.md](docs/vpc.md) · [PDF](docs/assets/vpc.pdf) |
| HMW définitif | [docs/hmw-definitif.md](docs/hmw-definitif.md) |
| Journal de prompts S2 (5 entrées) | [docs/journal-prompts-s2.md](docs/journal-prompts-s2.md) |
| Pitch HMW (2 min) | [docs/pitch-hmw.md](docs/pitch-hmw.md) |

## Feuille de route

| Séance | Étape | Statut |
|---|---|---|
| S1 | Empathize + Define : carte d'empathie, HMW | ✅ |
| S2 | Ideate : VPC, HMW définitif, journal de prompts | ✅ |
| S3 | Architecture multi-agents sur Dify | ⏳ |
| S4 | Prototype MVP avec Bolt.new | ⏳ |
| S6 | Démo intermédiaire | ⏳ |
| Juillet | Soutenance finale | ⏳ |

## Confidentialité

Ce dépôt est public : il ne contient **aucune donnée réelle de client** (noms, numéros de police, téléphones, montants individuels). Les exemples utilisés sont fictifs.
