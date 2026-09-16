# 3. Actions, planification et routeur

BaseActionsRouter reçoit une suite d’actions encodées. Le planner permet de construire un parcours comprenant plusieurs opérations : paiements, swaps, liquidité, transferts ou réglages.

Cette approche réduit les transactions intermédiaires mais rend le décodage critique. Chaque opcode doit être associé au bon format de paramètres et au bon ordre d’exécution.

V4Router spécialise cette mécanique pour les swaps et relie le règlement des deltas du PoolManager aux paiements effectifs. Multicall_v4 ajoute la composition de plusieurs appels dans un même contexte.

Le routeur ne doit pas être traité comme une garantie de prix : les bornes de slippage et les échéances restent des paramètres explicites de l’appelant.

Suite : [swaps et chemins](04-swaps-chemins.md).
