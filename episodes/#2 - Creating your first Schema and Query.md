Its time to create your first schema! 

Here I give an overview of the graphql-java-tools library which allows you 
to use the graphql schema language to build a graphql schema. This library 
takes a schema first approach and allows us to bring our own java object 
(matching the schema types) to fill in the implementation. This approach 
allows us to have complete control over the schema and have a good overview 
of what types are available.

Graphql tools by default will look for all **/*.graphqls files on the classpath 
and it will automatically combine and compile them into one graphql schema at 
application runtime. This is available at localhost:port/graphql/schema.json.

We then create our first graphql schema file with root type query.
Then we create a matching GraphqlQueryResolver which will match the root queries.
We then start graphql playground to view and play with our first graphql query.



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