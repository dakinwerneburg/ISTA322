# ASP.NET Core 3 Homework 07

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 3/21/2021

## 1. For the Sports Store application, what requirements does the author identify for implementation?
- an online product catalog that customers can browse by category and page 
- a shopping cart where users can add and remove products
- a checkout where customers can enter their shipping details
- an administration area that includes create, read, update, and delete (CRUD) facilities for managing the catalog
- protect it so that only logged-in administrators can make changes.

## 2. What is the purpose of the Startup class in ASP.NET Core applications?
- The Startup class is where services required by the app are configured, and the app's request handling pipeline is defined, as a series of middleware components.

## 3. What is the purpose of the CofigureServices method in the Startup class?
- The ConfigureServices method is used to set up objects, known as services, that can be used throughout the application and that are accessed through a feature called dependency injection.

## 4. What is a request pipeline and how does it work?
- The request pipeline is all the middleware components or processes that occur between initially receiving a request until a response has been submitted.  Each component can pass the request on to the next component or perform some work before and after.

## 5. What is the View Start class and how do we use it?
- The view start file tells Razor to use a layout file in the HTML that it generates, reducing the amount of duplication in views.  We use it using Razor syntax and declare and assign the default layout.

## 6. What is the feature in ASP.NET Core that generates the database schema for us? What does the file created by this feature contain?
- ASP.NET Entity framework Core uses a featured called migrations that generate the database schema.  The file that is created contains the SQL commands required to prepare the database.

## 7. When ASP.NET Core sees that a controller instance needs to be created, and that the controller object required another object that implements some interface, how does it determine which interface should be implemented?
- Using dependency injection it will look at the configuration in the startup class to see what the dependencies are and how they are created.

## 8. Explain how the paging mechanism works. How does the application calculate the number of pages required? How is this data passed to the view?
- Paging allows a certain number of items to appear on a page and provides links to the other pages.  It calculates the total pages buy taking the ceiling when you divide TotalItems by ItemsPerPage.  It is passed to the view from the controller as a parameter in the index method.

## 9. How does the book describe dependency injection? How is dependency injection used?
- Dependency injection decouple object instantiation from the code that is acting on it by providing a list of dependencies, and at the time of compilations will inject them as arguments to constructors and methods.  This allows much greater flexibility if there are changes in implementation.

## 10. How are the routes in MapDefaultControllerRoute() method arranged? Why is this important?
- Routes are processed in the order they are listed.  Since MapDefaultControllerRoute is general routing it should be last.
