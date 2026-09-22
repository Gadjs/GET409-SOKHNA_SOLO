# Journal de Prompts — Séance 1

Usage de l'IA documenté conformément au Code de déontologie IA du Lab GET 409 : l'IA assiste, les choix restent ceux de l'équipe.
Outil : Claude (interface web). Le journal des 5 prompts techniques de la séance 2 est dans [docs/journal-prompts-s2.md](docs/journal-prompts-s2.md).

| # | Objectif | Technique | Note |
|---|---|---|---|
| S1-P1 | Choisir le défi local | Zero-Shot | 4/5 |
| S1-P2 | Préparer le guide d'interview | Zero-Shot | 4/5 |
| S1-P3 | Structurer la carte d'empathie | Few-Shot | 4/5 |
| S1-P4 | Formuler les HMW | Zero-Shot → itération | 2/5 → 4/5 |

---

## S1-P1 — Choisir le défi local

**Prompt envoyé**
```
Tu es coach en innovation au Sénégal.
Contexte : je suis étudiante en Master et je travaille comme chargée de recouvrement chez NSIA Vie Assurances à Dakar. Je dois choisir un problème réel au Sénégal pour un projet de Design Thinking qui aboutira à un MVP avec IA.
Tâche : propose 3 problèmes que je peux observer directement dans mon travail, avec pour chacun l'utilisateur concerné et pourquoi il est pertinent.
Format : tableau en français (Problème | Utilisateur | Pertinence).
```

**Réponse IA (résumé)**
1) Retards de cotisation des assurés payant par Wave/Orange Money et relances manuelles (utilisatrice : la chargée de recouvrement). 2) Contrats commerciaux papier difficiles à retrouver pour payer les commissions (utilisateurs : contrôleurs). 3) Faible compréhension des produits d'assurance vie par les clients (utilisateurs : assurés).

**Note : 4/5** — Trois pistes réelles. **Choix de l'équipe : le problème 1**, parce que c'est la mission que je vis au quotidien, que j'ai accès au terrain et que l'impact se mesure (arriérés, contrats maintenus).

---

## S1-P2 — Préparer le guide d'interview

**Prompt envoyé**
```
Tu es expert en recherche utilisateur.
Contexte : je prépare deux interviews d'empathie de 5 minutes : une chargée de recouvrement d'assurance vie, et un assuré en retard de cotisation qui paie par Wave.
Tâche : rédige 6 questions ouvertes pour chaque interview, sans proposer de solution et sans orienter les réponses.
Format : deux listes numérotées en français.
```

**Réponse IA (résumé)**
Deux listes de questions ouvertes (« Racontez-moi… », « Que ressentez-vous quand… », « Racontez-moi la dernière fois que… »), sans questions fermées.

**Note : 4/5** — Conforme aux bonnes pratiques de la séance. J'ai ajouté une question sur les promesses de paiement, qui vient de mon expérience terrain. Résultat : [guide-interview.md](guide-interview.md).

---

## S1-P3 — Structurer la carte d'empathie (Few-Shot)

**Prompt envoyé**
```
Voici le format de carte d'empathie attendu :

Quadrant : ENTEND
Observation : « Le client dit qu'il a déjà payé par Wave »

Quadrant : VOIT
Observation : Des notifications de paiement sans lien avec le numéro de police

À partir de mes notes d'interview ci-dessous, classe chaque observation dans le bon quadrant (PENSE & RESSENT, ENTEND, VOIT, DIT & FAIT, PAINS, GAINS), avec le même format :
[notes d'interview de la chargée de recouvrement]
```

**Réponse IA (résumé)**
Classement des observations dans les 6 zones, au même format que les exemples.

**Note : 4/5** — Gain de temps sur le tri. Deux observations mal classées (un comportement mis dans « Pense ») ont été corrigées à la main. Résultat : [carte-empathie.md](carte-empathie.md).

---

## S1-P4 — Formuler les HMW

### Version 1
**Prompt envoyé**
```
Écris un HMW pour mon projet de recouvrement.
```
**Réponse IA (résumé)**
« Comment pourrions-nous créer une application mobile de recouvrement intelligente pour NSIA ? »

**Note : 2/5** — L'énoncé contient déjà une solution (« application mobile ») et ne dit ni pour qui, ni quel bénéfice : c'est exactement ce que la séance demande d'éviter.

### Version 2 (itération)
**Prompt envoyé**
```
Formule 3 énoncés HMW avec la structure : « Comment pourrions-nous [verbe d'action] pour [utilisateur] afin de [bénéfice] ? ».
Utilisateur principal : la chargée de recouvrement de NSIA Vie Assurances.
Insight : elle ne sait pas chaque matin quels assurés relancer en priorité, et les promesses de paiement se perdent.
Contrainte : aucun énoncé ne doit contenir de solution technologique.
```
**Réponse IA (résumé)**
Trois HMW centrés sur la priorisation des relances, le rattachement des versements aux contrats et le maintien des contrats des assurés à revenu irrégulier.

**Note : 4/5** — Bonne structure, sans solution imposée. Retravaillés et retenus dans [hmw.md](hmw.md).
