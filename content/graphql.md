---
created_at: 2023-01-09
type: concept
aliases: []
---

# GraphQL

## What is GraphQL?

- it is a query language, not specific to a [[database]].
- exists as a layer between the frontend and backend.
- prevents overfetching and underfetching of data between the frontend and backend, because the frontend can specify exactly what it wants.
- compared to rest.
	- only one endpoint.
- strictly typed, we define types to specify the data models in our application, should match the backend.
	- we can nest our custom types as lists within our other types.

## Queries.

- there is a special type in graphql called `Query`, which defines all of the possible queries that clients can make to fetch data.

```graphql
type Query {
	users: [User]
 
	# we can specify arguments that these queries take.
	# an exclamation mark means non-nullable.
	user(id: ID!): User
}
```

- we can also create `input` objects to organize the inputs to our queries into nameable types.

```graphql
input UserFilter {
	maxAge: Int
	minAge: Int
}

type Query {
	# we can pass our input as an argument to the query.
	# this query guarantees that an array (possibly empty) is returned.
		# if the array isn't empty, every value in it will be non-null.
	user(filter: UserFilter): [User!]!
}
```

- we can make a query by just calling this query by name and passing in the required arguments.
- we always have to specify the fields we want returned if the type of the field is not a primitive type.

```graphql
{
	user(maxAge: 50) {
		# we specify what fields we want returned here.
		# (assume these fields are defined on type User).
		id
		name
		age
	}
}
```

### Calling queries.

- to call a query in graphql, we use the following syntax.

```graphql
# this name is arbitrary.
query GetUser($maxAge: Int) {
	# this is the name of the query we defined on the graphql query type.
	user(maxAge: $maxAge) {
		id
		name
	}
}
```

## Mutations.

- we want to use the `input` keyword to define the shapes of the inputs that we expect for our mutations.
	- they allow us to set default values on fields in our definition.
	- often times, there’s virtual fields on our actual user types that we don’t expect a client to send when they are creating a new one.

## Resolvers.

- we define javascript functions on the global `resolvers` object, under the `Query` type, to define how queries should be run.
- in the same way, we can define them under the `Mutation` type to define how queries should run.

```javascript
const resolvers = {
	Query: {
		// this should match the name in graphql.
		user(parent, args) {
			// access arguments (args.maxAge, etc).
			// call db, do normal logic.
		}
	}
}
```

- we can also define resolvers under our own datatypes which will be called when that field is requested on the parent datatype.

```graphql
user {
	id
	name
 
	# logic for the movies here could be defined in a resolver scoped onto
	# the User type.
	favoriteMovies {
		title
		year
	}
}
```

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories::
