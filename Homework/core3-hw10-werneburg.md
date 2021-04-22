# ASP.NET Core 3 Homework 10

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 4/13/2021

## 1. What is Blazor?
- Blazor combines client-side JavaScript code with server-side code executed by ASP.NET Core, connected by a persistent HTTP connection.

## 2. What do the methods AddServerSideBlazor() and MapBlazorHub() do?
- The AddServerSideBlazor method creates the services that Blazor uses, and the MapBlazorHub method registers the Blazor middleware components.

## 3. Where are Blazor files conventionally located?
- They can be defined anywhere but conventionally is is located with the Pages folder.

## 4. What is the purpose of the Routed.razor file?
- This is Razor component will use the browser’s current URL to locate a Razor Component that can be displayed to the user

## 5. (Not in book) What is the purpose of the <NavLink> element, and what does it do?
- A component that renders an anchor tag, automatically toggling its 'active' class based on whether its 'href' matches the current URI without triggering a new HTTP request and losing the application state.

## 6. What is the purpose of an @code { ... } block? Where are they located and what is their purpose?
- The @code{...} is where the model for the view component lies and is located at the end of the razor page and is meant to map the values to the view at runtime.

## 7. How can a single component be configured to present two different sets of data without the need to duplicate code and content?
- It uses the same repository through Inject.

## 8. What is CRUD? What are the equivalent SQL statements?
- CRUD stands for Create, Read, Update, Delete and are standard operations in a database.  In SQL create is INSERT INTO, read is SELECT, update is UPDATE/SET, and delete is DELETE.

## 9. Does Blazor use the same approach to validation as the rest of ASP.NET Core? If not, how is Blazor different?
- Blazor uses the same approach to validation as the rest of ASP.NET Core but applies it a different way to deal with the more interactive nature of Razor Components.  It provides a set of built-in Razor Components that are used to display and validate forms, which is important because the browser can’t submit data using a POST request in a Blazor Component

## 10. What is the purpose of the Inject attribute?
- The Inject attribute declares that the specified interface must be implemented and is one of the ways that Blazor provides access to the application services.

## 11. What is the NavigationManager class? What does it do?
- NavigationManager class is what is used to programmatically navigate between components without triggering a new HTTP request.
