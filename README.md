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
    user(userId: "USER_ID") {
        userId
        age
        email
    }
}

# Get multiple users by IDs
query{
    users(userIds: ["USER_ID"]) {
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
  email: "hello@mail.com",
  age: 28}) {
    userId
    email
    age
    isSubscribed
  }
}

# Update user by ID
mutation{updateUser(updateUserData: {
    userId: "USER_ID"
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
        userId: "USER_ID"}) {
        userId
    }
}
```
