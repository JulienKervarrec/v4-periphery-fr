# 5. Deltas, règlements et actifs natifs

Le core v4 comptabilise les variations de soldes avant de demander leur règlement. DeltaResolver et Locker aident la périphérie à résoudre ces montants puis à transférer les actifs attendus.

Payments prend en charge les ERC-20 et la monnaie native enveloppée. NativeWrapper explicite le passage entre ETH et WETH, tandis que Permit2Forwarder sépare l’autorisation signée de l’exécution du transfert.

Cette comptabilité différée permet de composer plusieurs actions, mais elle impose de terminer le parcours avec des deltas soldés. Les callbacks et les contrats appelants doivent limiter la réentrance et vérifier le destinataire.

Les montants, frais et arrondis doivent être comparés dans les unités exactes du token.

Suite : [quoter et lecture](06-quoter-lecture.md).
