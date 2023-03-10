GraphQL is a query language for [[API]]s and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools.

*   Send a GraphQL query to your API and get exactly what you need, nothing more and nothing less.
*   GraphQL queries always return predictable results. 
*   Apps using GraphQL are fast and stable because they control the data they get, not the server.

```graphql
type Project {
	name: String
	tagline: String
	contributors: [User]
}
```


