![](https://github.com/Lylio/image-repo/blob/master/logos/apollo.png?raw=true)
![](https://github.com/Lylio/image-repo/blob/master/logos/graphql.png?raw=true)
![](https://github.com/Lylio/image-repo/blob/master/logos/nodejs.png?raw=true)

# Melody

### Description
Melody is a GraphQL Apollo server: https://melody-apollo-server.herokuapp.com/api


### Tech Stack
- Apollo Server
- GraphQL
- Node

### Setup & Launch

#### PostgreSQL-as-a-Container
A docker-compose file is available to spin up a Docker version of PostgreSQL if there isn't already a local instance running.
Execute the following command:  

`docker-compose up -d`

This instance of Postgres is configured to run on port 5433 - remember to update the database URL in the .env file if you plan
on using PostgreSQL this way.

#### Prisma
Prisma is a tool used to define the database schema. The schema file can be accessed and edited at src/prisma/schema.prisma.

NOTE - Each time this **schema.prisma** file is altered, the database migration command has to be executed:

`npx prisma migrate dev --name init`

This command has been included in the package.json script block so running `npm run migrate` will achieve the same result.

#### Prisma Studio
Prisma Studio is a simple GUI interface to explore and manipulate the data in the database (comparable to the H2 console). 
Simply run:
`npx prisma studio` and navigate to localhost:5555

#### NPM Launch
`npm run dev`

#### Query Instructions
Start the server with the above command, then navigate to localhost:4000/api and enter the playground by clicking on
'Query your server'. Run the following query:

```
query {
  boards {
    id
    title
    description
    path
  }
}
```

<br/>

#### Acknowledgements

- [TomRay.dev : *How to setup & deploy an Express GraphQL server with Apollo, Prisma, TypeScript, Postgres & Heroku*](https://tomray.dev/setup-and-deploy-graphql-server).
