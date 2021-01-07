###1 - Introduction, Dependencies

###2 - Creating your first Schema and Query

Ajouter la dépendance vers playground-spring-boot-starter.

Le "playground" graphql est ensuite disponible à l'url: http://localhost:8080/playground

Les schémas créé sont visibles en cliquant sur "SCHEMA".

On peut tester notre resolver avec la requête suivante:

{
  bankAccount(id: "dec054fe-3871-47c2-8188-9165f58a6095") {
    id
    name
    currency
  }
}

On obtient la réponse suivante :

{
  "data": {
    "bankAccount": {
      "id": "dec054fe-3871-47c2-8188-9165f58a6095",
      "name": "Georges",
      "currency": "USD"
    }
  }
}
