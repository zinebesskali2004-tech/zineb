# Analyse technique d'une transaction Bitcoin sur TestNet4
Nom et Prénom : Zineb Es-skali
## 1. Fiche d'identification

| Champ | Valeur |
|---|---|
| Réseau | Bitcoin TestNet4 |
| TXID | `0cd9b95e8af8a639e7d7c243f039699a66a898b1877b9915ac78dd06f7e97962` |
| Explorateur | [Mempool.space – ouvrir la transaction](https://mempool.space/testnet4/tx/0cd9b95e8af8a639e7d7c243f039699a66a898b1877b9915ac78dd06f7e97962) |
| Date et heure de consultation | À compléter |
| Statut observé | À vérifier |
| Hauteur du bloc | À compléter si confirmée |

## 2. Objectif et problématique

L'objectif est d'examiner la structure d'une transaction Bitcoin et d'expliquer comment elle consomme des sorties non dépensées (*Unspent Transaction Outputs*, UTXO) pour créer de nouvelles sorties.

**Problématique :** comment les entrées, les sorties et les frais permettent-ils de représenter un transfert de valeur dans le système Bitcoin ?

## 3. Relevé des données observables

Compléter ce tableau directement à partir de l'explorateur. Ne pas estimer les valeurs manquantes.

| Indicateur | Valeur à relever | Unité / remarque |
|---|---:|---|
| Nombre d'entrées | À compléter | inputs |
| Nombre de sorties | À compléter | outputs |
| Somme des entrées | À compléter | BTC ou satoshis |
| Somme des sorties | À compléter | BTC ou satoshis |
| Frais de transaction | À compléter | satoshis |
| Taille virtuelle | À compléter | vB, si affichée |
| Poids | À compléter | WU, si affiché |
| Taux de frais | À compléter | sat/vB, si affiché |
| Confirmations | À compléter | nombre au moment de la consultation |
| Bloc | À compléter si confirmé | hauteur |

**Moment de la vérification :** les confirmations et le statut peuvent évoluer. Indiquer la date et l'heure auxquelles les données ont été relevées.

## 4. Comprendre les entrées (Inputs)

Une entrée référence une sortie d'une transaction antérieure. Cette sortie antérieure doit être disponible et non dépensée au moment où la transaction est validée.

Pour chaque entrée, relever si l'explorateur les présente :
- le TXID de la transaction précédente ;
- l'index de sortie (*vout*) référencé ;
- le montant de la sortie consommée ;
- les informations de script ou d'adresse disponibles.

**Interprétation :** les entrées ne sont pas simplement des adresses qui envoient un solde. Elles désignent des sorties antérieures précises que la nouvelle transaction consomme.

## 5. Comprendre les sorties (Outputs)

Une sortie définit un montant et les conditions de dépense associées, généralement représentées par un script de verrouillage.

Pour chaque sortie, relever :
- l'index de sortie (*vout*) ;
- le montant ;
- l'adresse, si l'explorateur en affiche une ;
- le statut dépensé / non dépensé, si disponible.

Une sortie non dépensée constitue un UTXO qui pourra être référencé comme entrée d'une transaction future.

## 6. Modèle UTXO : lecture économique et technique

Le modèle UTXO fonctionne selon le principe suivant :

1. une transaction antérieure crée une ou plusieurs sorties ;
2. une nouvelle transaction référence certaines sorties encore non dépensées ;
3. ces sorties sont consommées comme entrées ;
4. la nouvelle transaction crée ses propres sorties ;
5. ces nouvelles sorties pourront être dépensées ultérieurement.

Le solde contrôlé par un portefeuille correspond à la somme des UTXO qu'il peut dépenser, et non à un chiffre unique stocké dans la blockchain comme dans un compte bancaire traditionnel.

### Schéma conceptuel

```text
Transactions précédentes
       |          |
     UTXO 1     UTXO 2
       \          /
        \        /
      Transaction étudiée
              |
        +-----+------+
        |            |
      UTXO A       UTXO B
   nouvelle sortie nouvelle sortie
```

Ce schéma illustre le modèle général. Il ne représente pas le nombre réel d'entrées ou de sorties de la transaction étudiée ; celui-ci doit être relevé dans l'explorateur.

## 7. Vérification des frais

Pour une transaction Bitcoin ordinaire, la relation de conservation de valeur s'écrit :

**Frais = Somme des entrées − Somme des sorties**

En satoshis :

- Somme des entrées : **[à compléter] sat**
- Somme des sorties : **[à compléter] sat**
- Frais calculés : **[à compléter] sat**
- Frais affichés : **[à compléter] sat**

Comparer le résultat calculé avec les frais indiqués par l'explorateur. Un écart peut provenir d'une erreur de relevé ou de conversion entre BTC et satoshis.

Rappel : **1 BTC = 100 000 000 satoshis**.

Les frais sont associés à la transaction et incitent les mineurs à inclure celle-ci dans un bloc. Ils ne constituent pas une sortie ordinaire vers le destinataire du paiement.

## 8. Taille et taux de frais

Lorsque les informations sont disponibles, relever la taille virtuelle (*virtual size*, vB) et le taux de frais.

**Taux de frais (sat/vB) = Frais (sat) ÷ Taille virtuelle (vB)**

Le taux de frais aide à comprendre la priorité relative proposée pour l'inclusion dans un bloc. Il ne faut pas confondre :
- le montant total des frais, exprimé en satoshis ;
- le taux de frais, exprimé en sat/vB.

Ne compléter cette partie qu'avec les données effectivement affichées.

## 9. Confirmation et inclusion dans un bloc

Une transaction diffusée peut être en attente dans la mempool. Lorsqu'elle est incluse dans un bloc accepté par le réseau, elle obtient une première confirmation. Les blocs ajoutés ensuite augmentent le nombre de confirmations.

À relever :
- statut au moment de la consultation ;
- nombre de confirmations ;
- hauteur du bloc, si confirmée ;
- date/heure du bloc, si affichée.

Le statut doit être daté, car il peut changer après la consultation.

## 10. Interprétation des résultats

Après avoir rempli le tableau de la section 3, rédiger une interprétation répondant aux questions suivantes :

1. Combien d'UTXO antérieurs la transaction consomme-t-elle ?
2. Combien de nouvelles sorties crée-t-elle ?
3. Les montants des entrées et sorties permettent-ils de retrouver les frais affichés ?
4. La transaction est-elle confirmée au moment de l'observation ?
5. Que peut-on conclure sur le rôle des UTXO dans cette transaction ?

**Résultat de l'analyse :** à rédiger après le relevé réel des données. Ne pas conclure sur des montants, des adresses ou des confirmations qui n'ont pas été vérifiés.

## 11. Limites de l'analyse

- Les informations de statut et de confirmation dépendent du moment de consultation.
- Certaines adresses ou certains scripts ne sont pas nécessairement présentés sous une forme lisible.
- L'analyse d'une seule transaction ne permet pas de généraliser à toutes les transactions Bitcoin.
- Les données doivent être relevées sur le réseau TestNet4 et ne doivent pas être confondues avec celles du réseau principal.

## 12. Conclusion

Cette étude présente les mécanismes essentiels d'une transaction Bitcoin : références aux UTXO antérieurs, création de nouvelles sorties, calcul des frais et confirmation par inclusion dans un bloc. L'explorateur permet de rendre ces éléments vérifiables publiquement.

La conclusion spécifique à la transaction étudiée devra être finalisée après la saisie des données observées dans le tableau de la section 3.

## 13. Références

- [Transaction étudiée – Mempool.space TestNet4](https://mempool.space/testnet4/tx/0cd9b95e8af8a639e7d7c243f039699a66a898b1877b9915ac78dd06f7e97962)
- [Documentation REST de Mempool.space – TestNet4](https://mempool.space/testnet4/docs/api/rest)
- Consignes pédagogiques du TP3 : *GitHub et projets blockchain*.
