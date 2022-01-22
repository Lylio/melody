![](https://github.com/Lylio/image-repo/blob/master/logos/apollo.png?raw=true)
![](https://github.com/Lylio/image-repo/blob/master/logos/graphql.png?raw=true)
![](https://github.com/Lylio/image-repo/blob/master/logos/nodejs.png?raw=true)

# Melody

### Description
Melody is a GraphQL Apollo server.
A demo can be found on Heroku: https://comingsoon.herokuapp.com

### Tech Stack
- Apollo Server
- GraphQL
- Node

### Setup & Launch

#### Node Launch
1. In the terminal, `node index.js`

A successful response is `🚀  Server ready at http://localhost:4000/
`

2. Navigate to http://localhost:4000
3. Click the **Query your server** link to enter the *Apollo Studio Sandbox*, then in the middle Operation pane, run the following query:

```
query GetBooks {
    books {
        title
        author
    }
} 
```

The result should be displayed in the right-hand side pane:

```
{
  "data": {
    "books": [
      {
        "title": "The Awakening",
        "author": "Kate Chopin"
      },
      {
        "title": "City of Glass",
        "author": "Paul Auster"
      }
    ]
  }
}

```

<br/>

#### Docker Launch
Coming soon

#### Query Instructions
Coming soon

<br/>

#### Acknowledgements

- [ApolloGraphQL.com : *Getting Started*](https://www.apollographql.com/docs/apollo-server/getting-started/)
