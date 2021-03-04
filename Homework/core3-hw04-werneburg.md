# ASP.NET Core 3 Homework 04

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 3/2/2021

## 1. What are the .NET SDK command line tools used for? Is their use required? Why or why not?
- .NET SDK command line tools provide all the necessary tools to creating, managing, building and running projects.  Many of the command line tools are can be done using an IDE but the command line could be done with less instructions, whereas some IDE templates would require more steps, depending on the IDE. 

## 2. What kind of applications do the following templates create? Run these commands and read the documentation. A brief summary of each template is sufficient.
> dotnet new console --help  *Create a new .NET Console application*
> dotnet new mvc --help      *Create a new .NET MVC application*
> dotnet new web --help   *Creates an project for creating web applications.*

## 3. What, specifically, do the following commands do?
> dotnet new globaljson --sdk-version 3.1.101 --output MySolution/MyProject
- creates a .json file located under the "MySolution/MyProject" directory with a key value pair that identifies the .NET SDK version of 3.1.101

> dotnet new web --no-https --output MySolution/MyProject --framework netcoreapp3.1
- Creates a emplty .NET Core 3.1 web application that does not support HTTPS and creates the files under the "MySolution/MyProject" directory

> dotnet new sln -o MySolution
- creates a solution file called, "MySolution".

> dotnet sln MySolution add MySolution/MyProject
- references the MySolution/MyProject directory to the MySolution file.


## 4. What is the purpose of the global.json file?
- Adding the global.json file ensures the right version of the .NET Core SDK will be used by the project.

## 5. What does the method app.UseStaticFiles() do?
- It adds support for responding to HTTP requests with static content in the wwwrootfolder.  I lets .NET know where it can find HTML, CSS, JavaScript and other resources for deployment.


## 6. What do the following two commands do?
> dotnet build
> dotnet run

- These are command line tools to build and run a .NET ASP application quickly.  If you use the dotnet run command it will build and run, whereas the build will just build.

## 7. (not in book) You can manage packages using the NuGet package manager and the command line tool dotnet add package. What are packages and what are they used for.
- Packages are third party libraries that can be referenced in your application to provide additional features.

## 8. What are tool packages and what are they used for?
- Tool packages install commands that can be used from the command line to perform operations on .NET Core projects

## 9. What are tool packages and what are they used for?

- Tool packages install commands that can be used from the command line to perform operations on .NET Core projects 

## 10. What are client side packages and what are they used for?

- client side packages are all the required content such as CSS and JavaScript

## 11. List two ways that a developer can debug code.
- You can use the IDE's debugger that provides a break in the execution and allows you step through each line of execution or you can use the Console.WriteLine to print out results to the console.  Another approach could be to do unit tests.