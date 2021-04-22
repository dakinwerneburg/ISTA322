# ASP.NET Core 3 Homework 11

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 4/20/2021

## 1. How are user authentication and authorization handled in ASP.NET?
- Authentication and authorization are provided by the ASP.NET Core Identity system.

## 2. What ASP.NET package supports the database functionality backing the identity system?
- Microsoft.AspNetCore.Identity.EntityFrameworkCore

## 3. In our Sports Store application, what is the connection string that allows access to our identity database?
- 
```c# 
"IdentityConnection": "Server=(localdb)\\MSSQLLocalDB;Database=Identity;MultipleActiveResultSets=true"
```

## 4. What methods are required to configure the middleware that supports user authentication and authorization?
- app.UseAuthentication();            
- app.UseAuthorization();

## 5. When you have multiple databases supporting one ASP.NET application, how do you ensure that specific components use the correct database?
- You Configure the IServices by using the AddDbContext method for each database you want to use. 

## 6. (not in book) In what namespace is the UserManager<T> class located? What is the purpose of the class? What interface(s) does the class require?
- Microsoft.AspNetCore.Identity and it requires IDisposable.

## 7. How are authentication credentials submitted to the application server? What services does the login manager use in submitting the authentication credentials?
- It is apart Identity framework and will generate standard authentication tables.  part of the scaffolding comes with /Account/Login which the application can use to prompt the user for their credentials.  UserManager<IdentityUser> and SignInManager<IdentityUser> are used in submitting authentication credentials.

## 8. How does an ASP.NET application determine the environment in which it is running?
- It checks it using the IWebHostEnvironment variable.

## 9. How do you define configuration settings for different environments, such as development or production?
- You use configure them using the appsettings.json file

## 10. (not in book) What is Docker? What is a container?
- Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels