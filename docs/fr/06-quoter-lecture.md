# 6. Quoter, StateView et lecture

V4Quoter estime le résultat d’un swap en rejouant une logique de routeur et en transportant le résultat par un revert contrôlé. QuoterRevert distingue ce retour prévu d’une erreur réelle.

StateView expose des informations du PoolManager utiles à l’interface et au suivi : état d’un pool, liquidité, ticks et paramètres. ReservesLens propose une vue spécialisée sur les réserves observables.

Ces contrats sont des outils de lecture et de simulation, pas une promesse d’exécution future. Un état peut changer entre la lecture, la signature et l’inclusion dans un bloc.

Un client fiable vérifie la chaîne, l’adresse du déploiement, le bloc de référence et les limites de slippage.

Suite : [hooks et pools permissionnés](07-hooks-pools.md).
