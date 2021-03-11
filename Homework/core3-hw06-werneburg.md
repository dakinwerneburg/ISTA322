# ASP.NET Core 3 Homework 06

-- Dakin Werneburg
-- MSSA Cloud Application Developer Certification
-- 3/8/2021

## 1. What is unit testing as defined by the book?
- Unit testing is isolating parts of your code and supplying it with an intial state by creating mock data and then performing some execution you want to test and check or Assert if the end state was what was expected or not.  According to the book these steps are broken down to Arrange, Act, and Assert.

## 2. What is the convention for creating unit tests in ASP.NET Core applications?
- Use the dotnet new command with the project template for your preferred test framework 
 

## 3. Name three unit test project tools used for ASP.NET Core applications.
> mstest
> nunit
> xunit

## 4. What is the convention for naming unit tests in ASP.NET Core applications?
- The convention is to create a separate project and name it with .Test extension.   

## 5. What is the convention for naming the test classes in AP.NET Core? What is the convention for naming the methods in the test classes?
- The convention is to name class that describe what your are testing and methods should have an attribute flag, what the attribute flag is depends on the testing framework.

## 6. What is the purpose of the Fact attribute in Xunit? (not in book) What is the purpose of the Theory attribute in Xunit?
- Both are used for unit testing but the Fact attribute takes no method arguments and Theory takes parameters.

## 7. Describe the different elements of the AAA testing pattern.
- Arrange is preparing the intial state of the test by supplying mock data; the Act is running the actual test by running some series of statements or a method; and the Assert is stating what the endstate is or the behavior that is expected using the mock data.

## 8. Describe the use of the methods in the Assert class. Describe the purpose, parameters, and return value of the Assert.Equals() method.
- Each Assert method allows different types of comparison to be made.  purpose of the Assert.Equals is to compare to objects to see if they have the same hash code.  The parameters for this method are the two objects that are being compared and must implement the IEqualityComparer<T> interface.  The return type is a bool.

## 9. What is the key to isolating a component for testing?
- The key to isolating a component is to remove dependencies by using interfaces to group behavior.

## 10. What is a mocking package? What does it do?
- Mocking package is a framework that the author uses to simplify the creating objects without defining a custom test class, which uses lambda expressions as arguments.

##  11. (not in book) What is the difference between the Setup() and the SetupGet() methods of Moq?
- Setup is used to mock a method or property and SetupGet is specifically for the getter of the property.