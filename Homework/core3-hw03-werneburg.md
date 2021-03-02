# ASP.NET Core 3 Homework 02

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 2/28/2021


## 1. What is the most important part of an ASP.NET Core 3 application?
- The Data model is the most important part.

## 2. What is the domain model?
- Domain model is just the model or C# object

## 3. Where are the model classes in an ASP.NET Core 3 application placed?
- In the Models Folder under the project folder

## 4. How many action methods can a controller class define?
- Multiple action methods but should be grouped into one controller class

## 5. What is a tag helper?
- A tag helper is an instruction for Razor that will be performed when the view is rendered.  It takes tags that asp understands and converts them to actual HTML tags

## 6. What does the asp-action attribute do?
- asp-action attribute maps the URL to the action method in the controller class.

## 7. What is the difference between HTTP GET and HTTP POST? This is an important question, and you should understand the difference.
- HTTP GET sends form data as key value pairs in the URL and is the default when making a request.  In a POST the data doesn't send the key value pair in the URL but is attached as a header.

## 8. What is model binding?
- model binding is linking key value pairs to the properties within a controller class.

## 9. Why should we validate user data? How do we validate user data?
- We should validate user data to ensure it binds to the model and for security reason to prevent cross-site scripting or SQL injection.

## 10. What, specifically, is the ModelState.IsValid property?
- ModelState.IsValid is flag on the controller class that checks to see if all the fields that were posted by the client matched the criteria set in the required section of the action method.

## 11. What does the asp-validation-summary do?
- asp-validation summary will convert a list of validations to HTML and if you want all you can specify the flag "All".

## 12. Static content consists of content such as images, script files, style files, etc. In an ASP.NET Core application, what is the name of the folder that contains static content?
- In ASP.NET Core all static content is stored in the wwwroot folder and should be subdivided further depending on the content.  User defined content should be under CSS; 3rd party CSS should be in lib folder, and JavaScript should be in js folder.


## 13. What is Bootstrap? Who developed Bootstrap? Is Bootstrap a proprietary package? If not, what is it?
- Bootstrap is a huge library of preconfigured CSS definitions that give responsive design and custom CSS that make building websites faster.  It was created by twitter and is open source.  
