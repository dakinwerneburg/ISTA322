# ASP.NET Core 3 Homework 09

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 4/6/2021

## 1. The text contains the following:
> I defined a Cart model class in the previous chapter and demonstrated how it can be stored using the session feature, allowing the user to build up a set of products for purchase. The responsibility for managing the persistence of the Cart class fell to the Cart Razor Page, which has to deal with getting and storing Cart objects as session data. The problem with this approach is that I will have to duplicate the code that obtains and stores Cart objects in any other Razor Page or controller that uses them.   
 
> In your own words, describe thee “problem” the author identifies and explain why the proposed solution is not satisfactory.
- The "problem" that the author referred to was object instantiation, using dependency injection and singleton provide more flexibility with object instantiation in addition session state will be lost if the application is restarted. 

## 2. What are services, and how do they work.  
- Services are interfaces or abstract classes and provide the blue print so more general classes can be used, allowing decoupling of specific classes.

## 3. (Not in book) The author states, “The static GetCart method is a factory for creating SessionCart objects and providing them with an ISession object so they can store themselves.” What does he mean by calling the GetCart method a factory?
- Factory method is responsible return a concrete class similar to dependency injection, but in this case, it uses dependency injection to instantiated the object, and using the GetCart method will check to see if a cart object is already instatiated and will return the singleton or will will create a new one.

## 4. What does the AddScoped method do?
- It is dependency injection system that will replace an Interface with a class the specified class that implements it at runtime.

# 5. How is an HTML form element with a tag handler of asp-page-handler programmed to execute the
functionality exposed by the form?

## 6. What does the BindNever attribute do? Why is it useful?
- BindNever prevents the front end user from entering data for an item like a primary key.  This is useful so primary keys are generated using auto increment or administrator defined.

## 7. What does the tag helper <asp-for> do?
- <asp-for> is tag helper that tightly couples the data type to the html element allowing for quick html generation.

## 8. Using Entity Framework, how do you add a new model to your database?
- Add a DBset to your context class then add migrations, it will check the difference and create the table.

## 9. What, specifically, does this command do: dotnet ef migrations add Model?
- It will create the schema for your Model

## 10. How does Entity Framework understand to load data that is contained in multiple tables? For example, suppose you want to load data from both Orders and Order.Details. What LINQ methods accomplish this?
- Entity framework uses Include and ThenInclude methods

## 11. Why do we validate data on the client side? Why do we validate data on the server side? What are the advantages and disadvantages of client side validation and server side validation?
- Since it takes more time talking to the server, especially when it busy, it best to catch validation errors locally using JavaScript.  The reason why we validate on the server side is for security reasons, as JavaScript can easily be manipulated in the browser.