* Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files.
* There are two types of ‘Helpers’.
    1. An HTML Helper is a method in the HTML page that returns a string. The string can represent any type of content. You can use HTML Helpers to render standard HTML tags like HTML <input> and <img> tags. HTML Helpers help to render complex content such as tab strips or HTML tables. The ASP.NET MVC framework includes: Html.ActionLink(), Html.BeginForm(), Html.CheckBox(), Html.DropDownList(), Html.EndForm(), Html.Hidden(), Html.ListBox(), Html.Password(), Html.RadioButton(), Html.TextArea(), Html.TextBox() and more.
    2. MVC Helper - ASP.NET Core Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files (.cshtml).  There are Tag Helpers for creating forms and links, loading assets, etc. Tag Helpers are written in C# and they target HTML elements based on element name, attribute name, or parent tag. Tag Helpers reduce the explicit transitions between HTML and C# in Razor views.  HTML Helpers provide an alternative approach to a specific Tag Helper and Tag Helpers don't replace all HTML Helpers.
* Tag Helpers vs HTML Helpers
    * Tag Helpers are preferable to HTML Helpers for a variety of reasons. They: are written in C# target HTML elements based on element name, attribute name, or parent tag reduce explicit transitions between HTML and C# provide a HTML-friendly environment because the syntax is familiar to front-end designers.  provide IntelliSense.  target standard HTML elements provide attributes created server-side on the model to the element.  
    * HTML Helpers can be used when a specific Tag Helper is unavailable. 
* <Form> Tag Helper
    * Must be used in conjunction with the asp-controller and asp-action Tag Helpers and the [ValidateAntiForgeryToken] attribute on the Action method. Automatically generates a hidden Request Verification Token to prevent cross-site request forgery (CSRF). The Alternative, Html.BeginForm, doesn't automatically include an anti-forgery token.
* <label> Tag Helper
    * The <label> tag helper <label asp-for="Name">, gives the label for a model value. It’s html helper equivalent is Html.LabelFor(). The <label> Tag Helper provides the following benefits over a pure HTML <label> element: Get the descriptive label value from the [Display] attribute in the Model. Less markup in the source code Strong typing with the Model Properties.
* <Input> Tag Helper
    * The <input> Tag Helper binds an HTML <input> element to a model expression. <input asp-for="Name" /> is equal to  @Html.EditorFor(m => m.Name) If a model is passed to the view, the form control will begin already populated with the model’s values. Generates HTML5 validation attributes from data annotation attributes applied to the models properties.
* Validation Message Tag Helper
    * Used for client-side validation and displays the results of server-side validation when a form is rejected. <span asp-validation-for=""> is equal to html helper Html.ValidationMessageFor() Leverages model data attributes and jQuery to display validation error messages in the body of the <span> element and prevent the form from being submitted.  It will also display server-side ModelState errors.
* Validation Summary Tag Helper
    * asp-validation-summary is equivalent to html helper Html.ValidationSummary(). also displays server-side ModelState errors. used to display a summary of validation messages. 
* <select> Tag Helper
    * The <select> tag helper is equal to Html.DropDownListFor(). You give it the list of items and the property to put the selected item into. The list should be an IEnumerable<SelectListItem> (e.g. SelectList) property on the model. 
* <a> (anchor) Tag Helper
    * The <a> Tag Helper is equal to Html.ActionLink(). It is used to create a link to specify a Controller/Action method.  If the asp-controller attribute is specified and asp-action isn't, the default asp-action value will be the Action associated with the currently executing View. asp-route-id enables a wildcard route prefix. Any value occupying the {value} placeholder in the URL is interpreted as a potential route parameter. If a default route isn't found, this route prefix is appended to the generated href attribute as a request parameter and value.
    