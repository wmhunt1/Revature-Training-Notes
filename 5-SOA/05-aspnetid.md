* ASP.NET Core Identity
    * Built in Authentication/Authorization service 
    * Adds UI to ASP.NET core web apps
    *  Adds the Database Configure Identity services app.UseAuthentication(); app.UseAuthorization(); ConfigureServices 
    * options.Cookie.HttpOnly = true;
* Scaffolding Identity
    * Right-click on the application in Visual Studio
    *  Choose “New Scaffold item” 
    * Choose Identity! 
    * You can now manipulate identity pages to meet your project requirements
* Manipulating a scaffolded identity page
    * Example: Triggering a “customer” account row to be added to database on initial external login success Note: To avoid unwanted dependencies between the ASPNetUsers table and my customer infrastructure, I built them as separate entities
* ASP.NET Identity - Pros & Cons
    * Pros: Easy to include into existing projects
    * Cons: Somewhat Challenging to Unit Test against - requires reasonably strong understanding of Identity Framework Incorporating Identity pages requires a lot of reworking scaffolded pages to meet specific application needs Requires specialized type of DbContext to incorporate identity 