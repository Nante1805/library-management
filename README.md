Partie 1:

1. Composants de pagination

Dans la spécification de l'OpenAPI, des composants ont été créés sous 'components/parameters' pour gérer la pagination au moyen de paramètres de requête (queryPagination pour les paramètres de requête et pathPagination pour les paramètres de chemin). Ces composants remplacent les paramètres de pagination utilisés dans les opérations GET /books et GET /authors.

2. Structure par défaut de la réponse d'erreur

Un composant de réponse d'erreur réutilisable (ErrorResponse) a été introduit sous components/responses pour définir la structure commune à toutes les réponses (200, 400, 403 et 500). Cette structure comprend un objet de statut avec des propriétés de code et de message, et un objet de corps contenant les valeurs de la réponse.

3. Importation de livres et d'auteurs

L'API prend désormais en charge l'importation de livres et d'auteurs à partir de deux formats de fichiers différents (Excel et JSON). Deux nouveaux points de terminaison ont été ajoutés : POST /books/import et POST /authors/import. Ces deux points de terminaison renvoient une liste d'éléments importés (livres ou auteurs). Le polymorphisme est utilisé pour gérer le choix du format de fichier (Excel ou JSON) à l'aide du mot-clé oneOf.

Lien de la première partie : https://github.com/Nante1805/library-management/tree/oas-td4-std22020-std22026?fbclid=IwAR2qeT_hVE98yebwtBdgZGEGOLeXHRjRj2uVB7ujWazZ6U7lR7V1Sr6pnUY

