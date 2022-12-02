## Repository and Unit of Work Pattern

The Repository pattern and Unit of Work pattern are used together most of the time. 

In this short summary I will make it clear how to implement and give a brief definition.

## Definition Repository

The Repository mediates between the domain and data mapping layers, acting like an in-memory collection of domain objects. [“Patterns of Enterprise Application Architecture” by, Martin Fowler]

When we are using a controller and want to do some manipulation on the database we use the DBContext through EF Core which represents a session with the database used in the project. What we have in this approach is a tight coupling between our controller and the EF Core framework, as the data access logic is in the EF Core of the DbContext.
Once we have a repository, we implement all data access logic in it and solve the decoupling problem.

conceptually it encapsulates a set of objects persisted in a datastore and the operations performed on them. Providing a more object-oriented view on the persistence layer.

![plot](./img/Captura%20de%20tela_20221201_212851.png)

## Definition Unit of Work

Maintains a list of objects affected by a business transaction and coordinates the writing out of changes.  [“Patterns of Enterprise Application Architecture” by Martin Fowler]

A unit of work tracks everything that is done during the business transaction that can affect the persistence layer.
When finished, she discovers everything that needs to be done to change the persistence layer as a result of the work.

![plot](./img/Captura%20de%20tela_20221201_215556.png)