# Idéation — Méthode des 6 Chapeaux de Bono

Point de départ : HMW 1 (S1) — prioriser les relances et réduire les arriérés.
Chaque chapeau exploré environ 3 minutes. Projet en solo : Sokhna porte les 6 chapeaux, la synthèse (chapeau bleu) est faite en tant que Chef de Produit.

## ⚪ BLANC — Les faits
- Une seule personne gère le recouvrement de tous les assurés qui paient par Wave et Orange Money.
- Chaque versement est saisi à la main dans la base de recouvrement avec le numéro de police.
- Plus de 20 millions FCFA déjà recouvrés par cette seule personne.
- Wave et Orange Money sont les moyens de paiement dominants au Sénégal ; les deux permettent d'exporter l'historique des transactions.
- Objectif de l'entreprise : créer un service dédié au recouvrement l'an prochain.

## 🔴 ROUGE — Les émotions
- Chargée : fierté des résultats, fatigue, peur de « rater » un client, stress des comptes rendus.
- Assuré : gêne d'être en retard, crainte de perdre l'argent déjà versé, agacement quand on le relance alors qu'il a payé.

## ⚫ NOIR — Les risques
- **Données personnelles** : les informations clients sont sensibles (loi sénégalaise 2008-12, CDP). Rien ne doit sortir de NSIA ni aller sur un dépôt public.
- Les exports Wave/OM n'ont pas toujours le numéro de police : rapprochement par numéro de téléphone ou montant, donc risque d'erreur.
- Une IA qui rédige des relances peut produire un ton maladroit ou une erreur de montant : validation humaine obligatoire.
- Adoption : si l'outil demande plus de saisie qu'Excel, il ne sera pas utilisé.

## 🟡 JAUNE — Les opportunités
- La base de recouvrement existe déjà : on part de données réelles.
- Le mobile money laisse une trace datée de chaque paiement.
- Un outil clair devient l'argument pour obtenir le service dédié (chiffres à l'appui).
- Maintenir un contrat coûte moins cher que d'en vendre un nouveau.

## 🟢 VERT — Les idées créatives (sans jugement)
1. Tableau de bord « Qui relancer aujourd'hui ? » trié par priorité.
2. Import des relevés Wave/OM et rapprochement automatique avec les numéros de police.
3. Score de risque de déchéance (jours de retard × montant × historique).
4. Messages de relance rédigés par IA, adaptés au client (ton, langue français/wolof), validés avant envoi.
5. Historique de chaque relance et des promesses de paiement, avec rappel à la date promise.
6. Rappel préventif SMS/WhatsApp 3 jours avant l'échéance.
7. Proposition d'échéancier fractionné pour les clients en difficulté.
8. Indicateurs mensuels automatiques pour la direction.
9. Lien de paiement Wave direct dans le message.
10. Chatbot vocal en wolof pour que l'assuré vérifie s'il est à jour.

## 🔵 BLEU — La synthèse (Chef de Produit)
**Retenu pour le MVP (V0) :** idées 1, 2, 3, 4, 5 et 8 → un tableau de bord de suivi du recouvrement.
**Plus tard (V1) :** idées 6, 7, 9 (demandent une intégration avec les opérateurs ou une validation de la direction).
**Écarté pour l'instant :** idée 10 (trop coûteuse pour la durée du cours).
