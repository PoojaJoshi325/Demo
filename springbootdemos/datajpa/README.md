# Spring data JPA demo implementation with example self notes

## Steps involved
###1. have the jpa starter dependency in the pom.xml file
###2. have the dependency corresponding to the database that you are using in pom.xml
###3. Define a Simple Entity

1.for this you need to create the POJO with getter and setter corresponding to a database table and annotate the POJO class with **@Entity** annotation.
  properties of the POJO are mapped to columns of the database table

2.If the database table name is different than the **@Table ** annotation to specify it otherwise just **@Entity**

3.for an auto generated id column use **@GeneratedValue(strategy=GenerationType.AUTO) ** 

4.there should be a protected default empty constructor for the sake of use of JPA.

5.there should be a parameterised constructor in case you want to create objects to be saved to database

###4. Create simple repository
In Spring data repository you do not need to code the crude logic of repository. Repository implementations are created automatically by Spring at runtime from a repository interface.
So, 
1.you'll have to create an Interface for the repository.
2.extent it from  CrudRepository<YourEntityClass, TypeOfTheIdPropertyOfEntityClass>
**CrudeRepository provides with several methods for working on crude operations saving, deleting, and finding**
3.declare the findBy and findAll methods
