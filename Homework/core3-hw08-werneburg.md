# ASP.NET Core 3 Homework 08

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 3/29/2021

## 1. For chapter 8 of the ASP.NET Core 3 book, what are the three requirements as the author describes them?
- Enhance the Index action method in the HomeController class so that it can filter the Product objects in the repository.
- Revisit and enhance the URL scheme
- Create a category list that will go into the sidebar of the site, highlighting the current category and linking to others

## 2. When adding new routes in Startup.cs, in what order should you add the new routes? Why?
- Routes must listed from top to bottom as the order in which routes execute, because this is how .NET checks the URL paths when a request comes in.

## 3. Does ASP.NET Core 3 handle outgoing HTTP requests as well as incoming requests? If so, what is one reason that this is important?
- Yes, ASP.NET Core 3 can handle outgoing requests and the reason why this is important is it give a much cleaner URL and no detail is added to the URL.

## 4. What is a view component? Why do you use view components?
- A view component is a C# class that provides a small amount of reusable application logic with the ability to select and display Razor partial views.


## 5. When you use a view component in a view, how is the view component referenced, and what naming convention do you use?
- A view component is referenced using XML with a namespace of VC and viewcomponent name hyphenated, without ViewComponent. 

## 6. When ASP.NET Core 3 needs to create a instance of a component, how does it know what value to give the new instance?
- By registering the app in the Startup.ConfigurationServices() method it will create an instance of a component through dependency injection.

## 7. How do ASP.NET Core 3 components get information about a user’s current HTTP request? Why would it be important for the component to get this information?
- One way to get information about a user's current HTTP request is register AddSession in the ConfigurationServices method to store session state.  Another way is to use ViewBag and create a property and assign the value.  This is important because the user's information is persistent across different requests. In the shopping cart app, this allows shopping cart to persist while going to different pages on site.


## 8. What does the PathAndQuery extension method do with an incoming HTTP request? What does the method do with the return value? What is the return value?
- The extension method generates a URL that the browser will be returned to after the cart has been updated, taking into account the query string, if there is one.

## 9. What is session state?
- Session state is data associated with a series of requests made by a user.

## 10. What three types does a session state store? Suppose you want to store data that has a type that session state does not store, is it possible to do so? If so, how do you do it?
- The only three types that session state store is int, string, and byte[]; however you can use extension methods to add functionality to the ISession interface.  You could also use ViewBag, but not recommended.