# ASP.NET Core 3 Homework 05

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 3/8/2021

## 1. What is the purpose of the null conditional operator? Does it apply to value types or reference types?  Why or why not?
- The null condition operator is to prevent nullpointerexceptions by checking if the value is null and if so will attempt to assign it to a variable.  This only applies to reference types, because value types only store values and cannot be null.

## 2. What is the null coalescing operator? What does it do? 
- The null coalescing operator is series of two question marks that denotes that if an expression results in a null value, it will assign a default value to the variable.  This makes it easier than displaying nulls or assigning nulls to a variable.

##  3. How is the null conditional operator different from a nullable type? What is the purpose of nullable types?
- null conditional operators are attached to objects where as nullable types are used against a data type.  The purpose of nullable types is let the compiler know that the variable may contain a null value.


## 4. When you create an automatic property and initialize the property with a value, can the value be changed later? Can another value be assigned to the property? Can the value be changed in the constructor?
- Assigning a value to an auto-implemented property doesn’t prevent the setter from being used to change the property later. Another value can be assigned to the property or changed in the constructor.

## 5. What is an object initializer and what is it for? What is an collection initializer and what is it for?
- object initializer allow you to create an object and sets the values for the properties rather than the default values and can be done without the need to do it in the constructor.  This mainly syntax sugar and keeps code concise.


## 6. What does the is keyword do?
- The "is" keyword does type checking to see if the type that is being accessed is of that type.

## 7. How are extension methods defined?
- Extension methods are defined like a regular method that has return type and name.  In the parameter, you use the "this" keyword followed by the class that you would like to extend and variable name to reference the instance of this class, then any other parameters the extension method requires.  Only classes that are in the same namespace can be extended.


## 8. What is implicit typing or type inference? How do you implement it?
- Because some class and the initialization of some classes can be very verbose, authors of C# and many languages provide the use of the "var" keyword instead of the data type.  Implicit typing or type inference is how var knows what data type to use.  It sees what data type is being assigned and inferences the variable must be of this data type.


## 9. What is a default implementation of an interface? What is the purpose of a default implementation of an interface?
- Default implementation of interface is adding default implementation.  This adds the flexibility and backward capability of adding new features to interfaces without modify all existing classes that implement it.  Although this could be done with an abstract class, the true purpose of default implementation is that you inherit from multiple interface but can only inherit once from an abstract class.

## 10. What are asynchronous methods? Why should we use them? How are they used?
- asynchronous methods use the "async" keyword in the method signature and prevents the CPU from locking up of long running processes, and is meant to notify all callers of the method that the asynchronous task is completed. Asynchronous methods are used to make sure a race condition doesn't occur and allows process to be done concurrently using multiple processor or cores.

## 11. When you use the await keyword, do you have to use the async keyword? Why or why not?
- Yes, you have to use the "async" keyword if you use the "await" keyword.  This is because without the async keyword callers of the method would have no way of being notified that this method is waiting on a task to be completed, and that's just what "await" does.  

## 12. (not in book) What is the yield keyword used for? How do you use it?
- Using the await and async keywords, results in the method return the results when it is all finished.  However, some process may take a long time or could contain an infinite amount of processes.  The "yield" keyword allows results to be returned as they are completed.  There are two ways to use the yield keyword.  Either you use it with the return statement or with the break statement.

## 13. What is the effect of using the nameof() expression?
- nameof returns the string literal of the name of code element such as the name of the class, method, variable, etc. This is especially useful than hardcoding to get the name such as using reflection or overriding the ToString method.