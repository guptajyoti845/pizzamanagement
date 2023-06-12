# Pizza Management API

This is a simple Node.js application that provides an API for managing pizzas and their toppings using GraphQL. It uses the Apollo Server library for creating the GraphQL server.


## Prerequisites

Make sure you have Node.js installed on your machine.

## Installation

1. Clone this repository or download the source code.

2. Navigate to the project directory.

3. Run the following command to install the required dependencies:


```npm install```

## Usage

To start the server, run the following command:

```npm start```

The server will start running at http://localhost:3000. 

You can access the GraphQL Playground by opening this URL in your web browser.


## API

The GraphQL API provided by this server allows you to perform the following operations:


## Query

1. pizzas(pizza: String): [Pizza]: Retrieves a list of pizzas. If a pizza argument is provided, it filters the pizzas by name. 
2. pizza(id: Int): Pizza!: Retrieves a single pizza by its ID.


## Mutation

1. createPizza(pizza: String, toppings: [ToppingInput!]!): Pizza!: Creates a new pizza with the specified name and toppings. 
2. updatePizza(id: Int!, pizza: String, toppings: [ToppingInput]): Pizza!: Updates an existing pizza with the specified ID, name, and toppings.

## Types

1. Pizza: Represents a pizza object with the following fields:
   1. id: Int!: The unique identifier of the pizza. 
   2. pizza: String!: The name of the pizza. 
   3. stock: Int!: The stock quantity of the pizza. 
   4. toppings: [Topping!]!: The toppings associated with the pizza.
   
2. Topping: Represents a topping object with the following fields:
    1. id: Int!: The unique identifier of the topping.
    2. topping: String!: The name of the topping.

3. ToppingInput: Represents an input object for creating or updating a pizza, with the following field:

   1. id: Int!: The ID of the topping.
   

## Database

 The application uses fake representations of pizza and topping records stored in memory. In a production environment, you would typically retrieve data from a real database instead.


## Dependencies

The application depends on the following npm packages:

1. **apollo-server**: A library for building GraphQL servers. 
2. **graphql**: The JavaScript reference implementation for GraphQL.


These dependencies are automatically installed when you run npm install.


## Author

This application was developed by Jyoti Gupta.


## License

This project is licensed under the ISC License.




