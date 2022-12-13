# Data Pagination

Data Pagination is a good practice pattern used in APIs, when we implement a method
Get is not advisable to return all the data present in the database. Imagine that the return is too big so you can crash your application layer.

To implement a data pagination just:


###  implement a class:
![plot](./img/ClassQuewryStringParamters.png)


### Soon after, create another class with the name referring to your controller:
![plot](./img/CategoriasParameters.png)


### In your interface of your IRepository you need to put the new method and then implement it:

![plot](./img/IRepository.png)

![plot](./img/ConcreteRepository.png)

### Just then modify your Get method:

![plot](./img/GetMethod.png)



