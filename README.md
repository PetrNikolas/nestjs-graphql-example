# NestJS and GraphQL example

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## GraphQL
```bash
open http://localhost:3000/graphql in browser
```

### Examples

#### Query
```graphql
# Get user by ID
query{
    user(userId: "2981ce4c-78fb-49bf-8d20-f9b1bfc5c4b0") {
        userId
        age
        email
    }
}

# Get multiple users by IDs
query{
    users(userIds: ["2981ce4c-78fb-49bf-8d20-f9b1bfc5c4b0"]) {
        userId
        age
        email
    }
}

# Get all users
query{
    users {
        userId
        age
        email
    }
}
```

#### Mutations
```graphql
# Create user
mutation{createUser(createUserData: {
  email: "hello@petrnikolas.com",
  age: 28}) {
    userId
    email
    age
    isSubscribed
  }
}

# Update user by ID
mutation{updateUser(updateUserData: {
    userId: "2981ce4c-78fb-49bf-8d20-f9b1bfc5c4b0"
    age: 29}) {
        userId
        email
        age
        isSubscribed
    }
}

# Delete user by ID
mutation{
    deleteUser(deleteUserData: {
        userId: "f14607d1-2f04-4d23-98c6-9b48adc15177"}) {
        userId
    }
}
```
