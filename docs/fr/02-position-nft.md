# 2. Positions de liquidité et NFT

PositionManager transforme une position de liquidité v4 en NFT ERC-721. Le jeton représente la configuration : pool, ticks de prix, liquidité et éventuelles données de hook.

Cette représentation permet de transférer ou d’autoriser une position sans confondre le propriétaire du NFT avec le détenteur des tokens de liquidité. Les bibliothèques PositionConfig et PositionInfoLibrary extraient les champs compacts utilisés par le contrat.

Les actions d’ajout et de retrait modifient la liquidité du pool puis mettent à jour les données associées au NFT. Une position hors de sa plage de ticks se comporte différemment d’une position active.

L’intégrateur doit conserver la cohérence entre identifiant de position, paramètres de pool et autorisation ERC-721.

Suite : [actions et routeur](03-actions-routeur.md).
