# TP3 - Projet Individuel : Analyse d'une Transaction Bitcoin TestNet4

* **Auteur :** Zineb Es-skali
* **N° Apogée :** 2436536
* **Formation :** Master FINTECH / Blockchain
* **Encadrant :** Pr. A. ELBASRI

---

## 1. Question et Sujet Choisis
Dans le cadre du Travail Pratique n°3 (TP3), ce dépôt présente l'étude et l'analyse technique d'une transaction réelle effectuée sur le réseau de test **Bitcoin TestNet4**. 

L'objectif est de décortiquer le fonctionnement d'une transaction moderne (Entrées, Sorties, UTXO, Frais, SegWit et Taproot) en s'appuyant sur les données publiques de la blockchain.

## 2. Démarche Suivie
1. **Réalisation et suivi de la transaction :** Exécution d'un transfert sur TestNet4 via un portefeuille compatible (Wasabi Wallet) et récupération de son identifiant unique (`TxID`).
2. **Exploration on-chain :** Inspection détaillée de la transaction sur l'explorateur de blocs `mempool.space` (réseau TestNet4).
3. **Analyse technique :** Extraction des métadonnées (taille virtuelle, poids, frais, scripts Taproot) et vérification de l'équilibre entre les entrées et les sorties (modèle UTXO).
4. **Publication et Versioning :** Création de ce dépôt public et gestion de l'historique des modifications via **GitHub Desktop** (commits distincts, synchronisation locale/distante avec *Push* et *Pull*).

## 3. Résultat Obtenu
Le dépôt contient un rapport analytique complet dans le fichier [`analyse_transaction.md`](./analyse_transaction.md). L'étude démontre comment le modèle UTXO sépare le montant initial en un paiement destinataire (`0,00309488 tBTC`) et un retour de monnaie (*change*), tout en optimisant les frais grâce aux technologies **SegWit** et **Taproot**.

## 4. Outils et Sources Utilisés
* **Explorateur Blockchain :** [Mempool.space (TestNet4)](https://mempool.space/testnet4) – Source des données brutes de la transaction.
* **Portefeuille utilisé :** Wasabi Wallet (environnement TestNet4).
* **Gestion de versions :** GitHub & GitHub Desktop.
* **Assistant IA :** Utilisé comme aide à la structuration du rapport Markdown et à la synthèse des explications techniques.
