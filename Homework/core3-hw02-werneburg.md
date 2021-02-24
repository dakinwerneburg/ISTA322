# ASP.NET Core 3 Homework 02

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 2/21/2021

## 1. What is the difference between Visual Studio and Visual Studio Code? 
- Visual Studio is a lightweight version of Visual Studio that is cross platform.  Visual Studio Code is an integrated development environment that offers many different tools that make developing applications easier such as intellisense and debugging.  

## 2. What is LocalDB?
- LocalDB is a file on the your local machine that acts as a database with no configuration to store information.  It makes it quick and easier to get up and running a database.  

## 3. What do these commands do?   
> **dotnet new globaljson --sdk-version 3.1.101 --output FirstProject**
- The first command creates a folder named FirstProject and adds to it a file named global.json, which specifies the version of .NET Core that the project will use; this ensures you get the expected results when following the examples

> **dotnet new mvc --no-https --output FirstProject --framework netcoreapp3.1** 
- Creates a new ASP.NET Core project using the MVC template.

## 4. What command do you use to build an ASP.NET project from the command line? What command do you use to run the project?  
- To build an ASP.NET project navigate to the folder where the .csproj is and enter: "dotnet build" and to run use "dotnet run"    

## 5. What is the purpose of an endpoint? 
- To handle incoming HTTP requests 

## 6. What is a controller?
- The controller class directs HTTPS request to an "Action" method within the Controller class that will handle the request.   

## 7. Where are actions defined? 
- Actions are methods that are defined in the Controller Class.  

## 8. What is the purpose of the routing system?  
 - The ASP.NET Core routing system is responsible for selecting the endpoint that will handle an HTTP request

## 9. Assume that your ASP.NET application runs in a browser with a URL like http://localhost:5000. List the three default routes configured by the ASP.NET Core routing system.
> /
> /Home
> /Home/Index      

## 10. What does the ViewResult object instruct ASP.NET Core to do?
- ViewResult object instructs ASP.NET Core to return the .cshtml (Razor Page) with the name that is the same as the action method in the Controller class.   

## 11. How does ASP.NET Core know what View is to be called from an action method? 
- It first uses the path to identify the Controller used, then looks in the Views folder for a path with the same name as the Controller and action; then loads that page.  

## 12. What is the job of an action method?  
- The job of the action method is to process the business logic then pass a view and any parameters to that view or other object.  

## 13. What is a view model?
- The view model is how data is passed between a request and a response using a simple class.