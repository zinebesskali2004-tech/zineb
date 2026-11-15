# Étude technique d'une transaction Bitcoin sur TestNet4
Nom et Prénom : Zineb Es-skali
Projet individuel – TP3 : GitHub et projets blockchai 
Master FinTech / Blockchain

## Résumé

Ce projet étudie une transaction Bitcoin identifiée par son TXID et consultable sur le réseau de test Bitcoin TestNet4. L'étude porte sur la structure de la transaction, le modèle UTXO, les entrées et sorties, les frais de transaction et les confirmations.

L'objectif est de présenter une démarche de vérification reproductible à partir d'un explorateur de blockchain et d'interpréter les informations observées.

## 1. Référence de la transaction

- **TXID :** `0cd9b95e8af8a639e7d7c243f039699a66a898b1877b9915ac78dd06f7e97962`
- **Réseau :** Bitcoin TestNet4
- **Explorateur :** [Consulter la transaction](https://mempool.space/testnet4/tx/0cd9b95e8af8a639e7d7c243f039699a66a898b1877b9915ac78dd06f7e97962)
- **Date de consultation :** à compléter lors de la vérification

**Important :** les données chiffrées de la transaction ne sont pas reproduites ici tant qu'elles n'ont pas été relevées et vérifiées sur l'explorateur. Les champs à compléter figurent dans `ANALYSE_TRANSACTION.md`.

## 2. Problématique

Comment une transaction Bitcoin mobilise-t-elle des sorties non dépensées (UTXO), crée-t-elle de nouvelles sorties et détermine-t-elle les frais nécessaires à son inclusion dans la blockchain ?

## 3. Méthodologie

1. Ouvrir la référence de la transaction sur l'explorateur TestNet4.
2. Vérifier le réseau et le TXID.
3. Relever les entrées et leurs références aux transactions précédentes.
4. Relever les sorties, leurs montants et leurs scripts/adresses lorsqu'ils sont affichés.
5. Comparer la somme des entrées et la somme des sorties.
6. Vérifier les frais, le statut de confirmation et les informations du bloc, le cas échéant.
7. Interpréter les résultats à l'aide du modèle UTXO.

## 4. Livrables

- `README.md` : présentation, problématique, méthodologie, outils et sources.
- `ANALYSE_TRANSACTION.md` : fiche de relevé, explications techniques, calculs et interprétation.

## 5. Outils et transparence

- **Mempool.space – TestNet4 :** consultation de la transaction.
- **GitHub / GitHub Desktop :** dépôt, versionnement et publication.
- **Assistant IA :** aide à la structuration et à la rédaction. Les données propres à la transaction doivent être vérifiées par l'étudiant sur l'explorateur.

## 6. Auteur

- Nom et prénom : zineb es-skali
- Filière : Master d'Excellence Finance Appliquée – Option FinTech
- Module : Blockchain

## 7. Sources

- [Transaction étudiée – Mempool.space TestNet4](https://mempool.space/testnet4/tx/0cd9b95e8af8a639e7d7c243f039699a66a898b1877b9915ac78dd06f7e97962)
- [Documentation de l'API REST Mempool.space – TestNet4](https://mempool.space/testnet4/docs/api/rest)
- Consignes du TP3 : *GitHub et projets blockchain*.

## 8. Publication GitHub

Le dépôt doit être public selon les consignes du TP individuel, et contenir le README ainsi qu'un livrable réel. Prévoir au moins deux commits distincts et explicites, puis vérifier que les fichiers et l'historique sont visibles sur GitHub.

Exemples de messages de commit :
- `Add project README and methodology`
- `Add detailed Bitcoin transaction analysis`

---
**Périmètre :** étude pédagogique sur un réseau de test. Ne jamais publier de phrase de récupération, clé privée, mot de passe ou jeton d'accès.
