# Coding challenge

## Background

We are a new eCommerce portal. In our database, we are starting to store products and carts (1 cart: N products) and we will provide
interfaces to manage them.

We need to provide the below capabilities:
- get all products
- get all products of a single cart
- add a product to a cart

## Challenge

1. Provide interface specifications for the above functions / capabilities.
2. Provide implementation of the formulated specifications.
3. You can assume the products as a static data structure that is initialised when your program runs.

## Language

Java

## Deliverables

Interface specifications, the source files and any test code – preferably in a github / bitbucket public repo.

The solution will be evaluated based on the following criteria:
* Correctness
* Code structure
* Data structures
* Extensibility
* Maintainability
* Test coverage
* Performance

# Solution

While a real commerce solution contains many levels of abstraction, in our simple example, we limited ourselves to only three levels. The topmost level is the façade. The facade interface specifies the three required methods. We do not use services, to get data, the facade calls directly DTO objects.
The DTO objects themselves refer to the nominal repository. 
A situation was simulated when the legacy repository code can return null.
The DTO objects demonstrate how to handle such cases.

For unit tests we used Spock Framework. 
This made it possible to generate specifications automatically.
