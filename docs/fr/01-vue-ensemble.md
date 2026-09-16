# 1. Vue d’ensemble de la périphérie Uniswap v4

La périphérie regroupe les contrats qui rendent le singleton PoolManager utilisable par des applications : routeurs, gestionnaires de positions, bibliothèques, quoter et vues de lecture.

Le dépôt ne remplace pas le cœur v4. Il traduit ses opérations de bas niveau en parcours contrôlables : initialiser un pool, ajouter ou retirer de la liquidité, exécuter un swap et régler les deltas.

Les contrats centraux à suivre sont PositionManager, V4Router, BaseActionsRouter et les lenses. Les interfaces décrivent les frontières entre intégration, comptabilité du core et actifs ERC-20 ou natifs.

La qualité d’une intégration dépend autant du décodage des actions et des contrôles de slippage que de l’appel final au PoolManager.

Suite : [position et NFT](02-position-nft.md).
