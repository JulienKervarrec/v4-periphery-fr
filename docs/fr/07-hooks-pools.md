# 7. Hooks, permissions et pools spécialisés

La périphérie fournit des adaptateurs pour des pools dont le hook impose des règles supplémentaires. PermissionsAdapter et son factory encapsulent la relation entre allowlist, routeur et gestionnaire de positions.

Un hook peut intervenir avant ou après une action de liquidité ou de swap. L’intégration doit donc tenir compte des callbacks, des données hookData et des droits effectifs du caller.

Les pools permissionnés montrent une conséquence importante de l’extensibilité : deux PoolKey proches peuvent avoir des conditions économiques et d’accès différentes.

Les contrats d’application doivent refuser les hooks inattendus, contrôler les adresses et ne jamais déduire une permission de la seule présence d’un pool.

Suite : [sécurité et limites](08-securite-limites.md).
