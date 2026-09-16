# 4. Swaps, chemins et tolérance de prix

Les swaps v4 peuvent traverser plusieurs pools. PathKey encode la monnaie intermédiaire, la fee, la graduation de prix et l’adresse du hook nécessaire à chaque étape.

Le routeur exécute les étapes et compare le résultat à une quantité minimale ou maximale. SlippageCheck centralise les garde-fous pour éviter qu’une variation de prix transforme un appel valide en perte non acceptée.

Les montants négatifs ou positifs sont interprétés comme des deltas à régler auprès du singleton. Une erreur de signe, de monnaie ou d’ordre de chemin peut inverser le comportement économique.

Les chemins doivent donc être construits à partir de pools réellement compatibles et vérifiés avant signature.

Suite : [deltas et paiements](05-deltas-paiements.md).
