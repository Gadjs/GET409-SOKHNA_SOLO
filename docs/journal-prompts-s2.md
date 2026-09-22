# Journal de Prompts — Livrable S2

Outil : Claude (interface web). Projet : RecouvIA — recouvrement des cotisations d'assurance vie payées par Wave / Orange Money.
Règle suivie : si la note est inférieure à 3/5, le prompt est reformulé et les deux versions sont documentées.

| # | Technique | Note | Itération |
|---|---|---|---|
| P1 | Zero-Shot | 4/5 | Non |
| P2 | Zero-Shot | 2/5 → 4/5 | Oui (v1 → v2) |
| P3 | Few-Shot | 4/5 | Non |
| P4 | Chain-of-Thought | 5/5 | Non |
| P5 | Libre (rôle + contraintes + format JSON) | 4/5 | Non |

---

## P1 — Zero-Shot : les 3 problèmes du persona

**Prompt envoyé**
```
Tu es consultant en assurance vie et en recouvrement en Afrique de l'Ouest.
Contexte : chez NSIA Vie Assurances à Dakar, une seule chargée de recouvrement suit tous les assurés qui paient leurs cotisations par Wave et Orange Money. Elle relance les retardataires et saisit chaque versement à la main dans une base Excel avec le numéro de police.
Tâche : identifie les 3 principaux problèmes de cette chargée de recouvrement.
Format : réponds sous forme de liste numérotée en français, chaque problème en 2 phrases maximum avec sa conséquence sur les arriérés.
```

**Réponse IA (résumé)**
1) Pas de visibilité en temps réel sur les impayés, donc relances tardives et contrats qui tombent en déchéance. 2) Rapprochement manuel des paiements mobile money avec les polices, source d'erreurs et de relances inutiles. 3) Charge concentrée sur une seule personne, donc portefeuille partiellement couvert.

**Note : 4/5** — Pertinent et bien formaté, cohérent avec la carte d'empathie. Il manque le problème d'historique des relances (promesses de paiement oubliées), que j'ai ajouté moi-même au VPC.

---

## P2 — Zero-Shot : 5 idées de fonctionnalités pour le MVP

### Version 1
**Prompt envoyé**
```
Donne-moi 5 idées d'application pour le recouvrement.
```
**Réponse IA (résumé)**
Idées génériques : application mobile de paiement, blockchain pour tracer les dettes, chatbot, portail client, intelligence artificielle prédictive. Rien de lié à l'assurance vie, ni à Wave/OM, ni à une utilisatrice seule.

**Note : 2/5** — Trop vague : pas de rôle, pas de contexte, pas de format. Certaines idées (blockchain) sont hors de portée d'un MVP.

### Version 2 (itération)
**Prompt envoyé**
```
Tu es Product Owner d'une startup SaaS à Dakar.
Contexte : je construis un MVP pour une chargée de recouvrement de NSIA Vie Assurances qui suit seule les assurés payant par Wave et Orange Money. Son besoin principal : savoir chaque jour qui relancer en priorité et garder l'historique des relances.
Tâche : propose 5 fonctionnalités pour ce MVP, réalisables en 4 semaines avec un outil no-code / low-code.
Format : tableau en français avec les colonnes Fonctionnalité | Problème résolu | Priorité (Must / Should / Could).
```
**Réponse IA (résumé)**
1) Liste priorisée des retards (Must). 2) Import CSV des relevés Wave/OM et rapprochement par numéro de police (Must). 3) Fiche client avec journal des relances et promesses (Must). 4) Génération de messages de relance par IA à valider (Should). 5) Tableau d'indicateurs mensuels (Should).

**Note : 4/5** — Directement exploitable : c'est le périmètre retenu pour le MVP V0. Il manque l'alerte « promesse de paiement échue », ajoutée dans la fonctionnalité 3.

---

## P3 — Few-Shot : défi → solution

**Prompt envoyé**
```
Voici des exemples de défis de recouvrement et de solutions adaptées au contexte sénégalais :

Défi : Un assuré oublie sa date d'échéance chaque mois.
Solution : Rappel SMS automatique 3 jours avant l'échéance, avec le montant exact et le numéro Wave de paiement.

Défi : Un assuré affirme avoir payé mais le versement n'apparaît pas dans la base.
Solution : Recherche du paiement dans le relevé Wave/OM par numéro de téléphone et montant, puis rattachement au bon numéro de police avant toute relance.

Défi : Un commerçant du marché Sandaga a perdu une partie de ses revenus pendant 2 mois et a cessé de cotiser, alors qu'il veut garder son contrat.
Solution :
```

**Réponse IA (résumé)**
Proposer un échéancier de rattrapage fractionné (par exemple la dette étalée sur 4 mois en plus de la cotisation courante), envoyé par message bienveillant en wolof et en français, avec un suivi des promesses dans l'outil et un rappel à chaque échéance du plan.

**Note : 4/5** — Même format et même niveau de détail que les exemples : le Few-Shot a bien imposé le pattern. À valider avec la direction (règles internes sur les échéanciers).

---

## P4 — Chain-of-Thought : cause → obstacle → solution

**Prompt envoyé**
```
Tu es un expert en assurance vie et en inclusion financière en Afrique de l'Ouest.
Analyse le problème suivant : chez NSIA Vie Assurances à Dakar, les assurés qui cotisent par Wave ou Orange Money accumulent des retards, et une seule chargée de recouvrement ne parvient pas à les relancer à temps.
Réfléchis étape par étape :
Étape 1 : Identifie la cause principale du problème dans le contexte de Dakar.
Étape 2 : Décris l'obstacle principal qui empêche une solution classique (recruter, relancer plus) de fonctionner.
Étape 3 : Propose une solution technologique accessible à cette chargée de recouvrement, sans compétence en programmation.
Développe chaque étape avant de conclure.
```

**Réponse IA (résumé)**
Étape 1 — Cause : les revenus des assurés sont souvent irréguliers et le paiement mobile rend la cotisation facile mais aussi facile à oublier ; côté assureur, les paiements ne sont pas reliés automatiquement aux contrats, donc les retards sont détectés tard.
Étape 2 — Obstacle : recruter coûte cher tant que le service n'a pas prouvé sa rentabilité, et relancer plus sans priorisation épuise la chargée sans cibler les contrats les plus à risque.
Étape 3 — Solution : un tableau de bord qui importe les relevés Wave/OM, rapproche les paiements des polices, calcule un score de priorité et prépare des messages de relance, avec des indicateurs pour justifier ensuite le recrutement.
Conclusion : commencer par la visibilité et la priorisation, avant l'automatisation des envois.

**Note : 5/5** — Raisonnement vérifiable à chaque étape, ancré dans le contexte réel, et qui confirme le HMW définitif. C'est le prompt le plus utile de la séance.

---

## P5 — Libre : génération d'un message de relance (rôle + contraintes + format JSON)

**Prompt envoyé**
```
Tu es l'assistant de relance de NSIA Vie Assurances. Tu rédiges des messages courts, polis et rassurants, jamais menaçants.
Données du client (fictives) :
- Prénom : Moussa
- Retard : 2 cotisations mensuelles
- Montant dû : 30 000 FCFA
- Canal de paiement habituel : Wave
- Dernière promesse : paiement le 15 du mois, non tenue
Contraintes :
- 300 caractères maximum par message
- Une version en français et une version en wolof
- Rappeler que le contrat protège sa famille
- Proposer d'appeler si le client a une difficulté
Format de sortie : JSON avec les clés "francais", "wolof", "ton", "action_suivante".
```

**Réponse IA (résumé)**
Un JSON valide avec un message en français (« Bonjour Moussa, … vos 2 cotisations de 30 000 FCFA restent à régler … votre contrat protège votre famille … appelez-nous si vous avez une difficulté »), une version en wolof, un ton « bienveillant » et une action suivante « rappeler dans 3 jours si pas de paiement ».

**Note : 4/5** — Format JSON respecté, donc réutilisable dans un agent Dify en S3. La version en wolof doit être relue par une personne wolophone avant tout usage réel.

---

## Ce que j'ai appris
- Un prompt sans rôle, contexte ni format (P2 v1) donne des réponses génériques et inutilisables.
- Le Few-Shot impose un style et un niveau de détail sans avoir à tout expliquer.
- Le Chain-of-Thought produit l'analyse la plus fiable et la plus facile à vérifier.
- Demander une sortie JSON prépare directement la construction des agents Dify.
- Les données clients utilisées dans les prompts sont fictives : aucune donnée réelle de NSIA n'est envoyée à une IA.
