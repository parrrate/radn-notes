# CryptoCurrency Model
## Objects
### Subject
* Public key
### Signature
### Value
* Integer (variable length)
### Coin Data
* Subject + Value
* Data is valid iff subject is syntactically valid (i.e. of correct length) and value is resolvable (i.e. exists)
### Coin
* Coin Data + Origin Transaction
* Coin's validity depends solely on its data. Transaction reference is volatile and is allowed to be invalid.
### Transaction Data
* Set of Input Coins
* Set of Out Coins' Datas
* Data is valid iff both sets are structurally valid and all coins' datas are valid.
### Transaction
* Transaction Data
* Subject-Signature Mapping (signatures of data)
* Transaction is valid iff all signatures are valid, data is valid and each inputs' subject is present in the mapping.
### Bank
* Set of Input (Spent) Coins
* Set of Output (Minted) Coins
* Intersection of those two sets, Final Coins
* Multimapping InputCoin-Transaction (transaction where coin was used)
* Circulation is a Output\\Input difference, and its total value is called deficit
### Singleton Block
* Transactions + Bank
### Union Block
* Blocks + Bank
* Note: Union's Final Coins are not a union of block's Final Coins, i.e. it's an intersection of unions, not a union of intersections.
