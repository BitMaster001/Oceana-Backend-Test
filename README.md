# Oceana GraphQL Back-End test
type News {
    title: String
    date: String
    author: String
    likes: Int
    uuid: String
    text: String
}
type Query {
    "A query returning news list"
    news: [News]
    "A query returning a single news"
    singleNews(uuid: String!): News
}
type Mutation {
    "A mutation to like the news"
    like(uuid: String!): News
    "A mutation to dislike the news"
    dislike(uuid: String!): News
    "A mutation to delete the news"
    delete(uuid: String!): [News]
}

Implement a Node.js server using the above GraphQL schema.
Every Query and Mutation should work correctly.

## How to run project
- yarn
- yarn start
- open browser at http://localhost:4000/graphql