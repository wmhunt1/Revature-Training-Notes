Javascript
XSS
Cross-Site Scripting
a code injection attack that allows an attacker to execute malicious JavaScript in another user's browser
The attacker does not directly target his victim. Instead, he exploits a vulnerability in a website that the victim visits, in order to get the website to deliver the malicious JavaScript for him. To the victim's browser, the malicious JavaScript appears to be a legitimate part of the website, and the website has thus acted as an unintentional accomplice to the attacker.
The only way for the attacker to run his malicious JavaScript in the victim's browser is to inject it into one of the pages that the victim downloads from the website. This can happen if the website directly includes user input in its pages, because the attacker can then insert a string that will be treated as code by the victim's browser
Consequences of malicious JS:
Cookie theft
The attacker can access the victim's cookies associated with the website using document.cookie, send them to his own server, and use them to extract sensitive information like session IDs.
Keylogging
The attacker can register a keyboard event listener using addEventListener and then send all of the user's keystrokes to his own server, potentially recording sensitive information such as passwords and credit card numbers.
Phishing
The attacker can insert a fake login form into the page using DOM manipulation, set the form's action attribute to target his own server, and then trick the user into submitting sensitive information.
DOM
 Document Object Model
 a programming interface for HTML and XML documents
represents the page so that programs can change the document structure, style, and content.
The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.
data representation of the objects that comprise the structure and content of a document on the web. 
it's written in JavaScript, but it uses the DOM to access the document and its elements. The DOM is not a programming language, but without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, XML documents, and their component parts (e.g. elements).
Fundamental Data Types
Document
When a member returns an object of type document (e.g., the ownerDocument property of an element returns the document to which it belongs), this object is the root document object itself. The DOM document Reference chapter describes the document object.
Node	
Every object located within a document is a node of some kind. In an HTML document, an object can be an element node but also a text node or attribute node.
Element	
The element type is based on node. It refers to an element or a node of type element returned by a member of the DOM API. Rather than saying, for example, that the document.createElement() method returns an  object reference to a node, we just say that this method returns the element that has just been created in the DOM. element objects implement the DOM Element interface and also the more basic Node interface, both of which are included together in this reference. In an HTML document, elements are further enhanced by the HTML DOM API's HTMLElement interface as well as other interfaces describing capabilities of specific kinds of elements (for instance, HTMLTableElement for <table> elements).
NodeList	
A nodeList is an array of elements, like the kind that is returned by the method document.getElementsByTagName(). Items in a nodeList are accessed by index in either of two ways:
list.item(1)
List[1]	
These two are equivalent. In the first, item() is the single method on the nodeList object. The latter uses the typical array syntax to fetch the second item in the list.
Attribute	
When an attribute is returned by a member (e.g., by the createAttribute() method), it is an object reference that exposes a special (albeit small) interface for attributes. Attributes are nodes in the DOM just like elements are, though you may rarely use them as such.
NamedNodeMap	
A namedNodeMap is like an array, but the items are accessed by name or index, though this latter case is merely a convenience for enumeration, as they are in no particular order in the list. A namedNodeMap has an item() method for this purpose, and you can also add and remove items from a namedNodeMap.
 In simple terms, the window object represents something like the browser, and the document object is the root of the document itself. Element inherits from the generic Node interface, and together these two interfaces provide many of the methods and properties you use on individual elements. These elements may also have specific interfaces for dealing with the kind of data those elements hold
Given a DOM node, we can go to its immediate neighbors using navigation properties.
There are two main sets of them:
For all nodes: 
parentNode, childNodes, firstChild, lastChild, previousSibling, nextSibling.
For element nodes only: 
parentElement, children, firstElementChild, lastElementChild, previousElementSibling, nextElementSibling.
Some types of DOM elements, e.g. tables, provide additional properties and collections to access their content.
Ajax
 Asynchronous JavaScript And XML
 what it really means is, making HTTP requests and receiving responses from the browser via javascript
XmlHttpRequest
Use XMLHttpRequest (XHR) objects to interact with servers. 
You can retrieve data from a URL without having to do a full page refresh. This enables a Web page to update just part of a page without disrupting what the user is doing.
can be used to retrieve any type of data, not just XML.
success; the "xhr.response" property now has the response body.
if the response body is in JSON, we have JSON serializer
JSON.stringify() serializes
JSON.parse() deserializes
XMLHttpRequest.onreadystatechange
An EventHandler that is called whenever the readyState attribute changes.
XMLHttpRequest.readyState Read only
Returns an unsigned short, the state of the request.
indicates progress through request-response cycle means, 4 means response is loaded
XMLHttpRequest.response Read only
Returns an ArrayBuffer, Blob, Document, JavaScript object, or a DOMString, depending on the value of XMLHttpRequest.responseType, that contains the response entity body.
XMLHttpRequest.open()
Initializes a request. This method is to be used from JavaScript code; to initialize a request from native code, use openRequest() instead.
XMLHttpRequest.send()
Sends the request. If the request is asynchronous (which is the default), this method returns as soon as the request is sent.
Promises
 a Promise is an object that represents some result that can either:
succeed and arrive ("resolve")
 or fail with some error ("reject")
 when you have a Promise, you call one of two methods on it
.then(success, fail)   -> for success or failure
.catch(fail)           -> for failure
Fetch API
fetch returns a promise of the response headers
provides a generic definition of Request and Response objects
The fetch() method takes one mandatory argument, the path to the resource you want to fetch. It returns a Promise that resolves to the Response to that request, whether it is successful or not. 
Once a Response is retrieved, there are a number of methods available to define what the body content is and how it should be handled
CORS
Cross-Origin Resource Sharing (CORS) is a mechanism that uses additional HTTP headers to tell browsers to give a web application running at one origin, access to selected resources from a different origin
 XMLHttpRequest and the Fetch API follow the same-origin policy.
This means that a web application using those APIs can only request resources from the same origin the application was loaded from, unless the response from other origins includes the right CORS headers.
For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts.
Events
HTML events are "things" that happen to HTML elements.
Event Listeners 
The addEventListener() method attaches an event handler to the specified element.
The addEventListener() method attaches an event handler to an element without overwriting existing event handlers.
You can add many event handlers to one element.
You can add many event handlers of the same type to one element, i.e two "click" events.
You can add event listeners to any DOM object not only HTML elements. i.e the window object.
The addEventListener() method makes it easier to control how the event reacts to bubbling.
When using the addEventListener() method, the JavaScript is separated from the HTML markup, for better readability and allows you to add event listeners even when you do not control the HTML markup.
You can easily remove an event listener by using the removeEventListener() method
Some examples discussed in trainer code
Window.onload 
Runs when whole window is loaded
window.addEventListener('load', function ())
Better way of declaring same event handler as above
document.addEventListener('DOMContentLoaded', function ())
Event doesn’t wait as long as those above
 textElement.innerHTML = 'text modified from script'
Propagation
Event propagation is a way of defining the element order when an event occurs. If you have a <p> element inside a <div> element, and the user clicks on the <p> element, which element's "click" event should be handled first?
There are two ways of event propagation in the HTML DOM:
Bubbling
In bubbling the inner most element's event is handled first and then the outer: the <p> element's click event is handled first, then the <div> element's click event.
Capturing
In capturing the outer most element's event is handled first and then the inner: the <div> element's click event will be handled first, then the <p> element's click event.
Node
Node.js is an open source server environment.
Node.js allows you to run JavaScript on the server
Node.js uses asynchronous programming!
Node.js files contain tasks that will be executed on certain events
A typical event is someone trying to access a port on the server
Node.js files must be initiated on the server before having any effect
NPM
NPM is a package manager for Node.js packages, or modules if you like.
Node package manager, a tool used to build and configure a node application
npm CLI
CLI used to run commands concerning node.js
Package.json
Describes your module
Scripts
Contains build instructions for some project that compiles using Node.js
Semver
Semantic Version
Syntax: Major.minor.patch
Major: any breaking change
Minor: any new features
Patch: any bugfix/anything else
^ means versions between current and next major 
~ means versions between current and next minor
TypeScript
It is a typed superset of Javascript that compiles to plain JavaScript.
All valid JS is valid TS
a typed language, where we can specify the type of the variables, function parameters and object properties.
Makes JS strongly typed
Uses type inference
Type annotations
We can specify the type using :Type after the name of the variable, parameter or property.
includes all the primitive types of JavaScript- number, string and boolean.
used to enforce type checking
type annotations help the compiler in checking types and helps avoid errors dealing with data types
Interfaces
Interface is a structure that defines the contract in your application
defines the syntax for classes to follow
Used for type checking
also known as "duck typing" or "structural subtyping"
Used for model binding
also used to define a type of a function
We can have optional properties, marked with a "?". In such cases, objects of the interface may or may not define these properties.
Classes
Like Java and C#
Can also be used for model binding and type checking
Modules
Modules are a way to create a local scope in the file. So, all variables, classes, functions, etc. that are declared in a module are not accessible outside the module. 
A module can be created using the keyword export and
A module can be used in another module using the keyword import
Transpilation
Converting typescript code to js
Tsc
Transpiler that converts ts to js
Tsconfig.json
TypeScript supports compiling a whole project at once by including the tsconfig.json file in the root directory.
a simple file in JSON format where we can specify various options to tell the compiler how to compile the current project.
Webpack
used to compile JavaScript modules
Module bundler
Basically converts all your modules to one big happy JS file
Webpack.config.js
For proper usage and easy distribution of this configuration, webpack can be configured with webpack.config.js. Any parameters sent to the CLI will map to a corresponding parameter in the config file.
How to run your webpack bundle
Angular
A front end fw used to create SPAs. Modularized in nature, front end design revolves around the idea of components making up a page. 
Single-page application
a single page application literally has only one page
Single Page Applications are super easy to deploy in Production, and even to version over time!
Module
Angular’s own modularity system
containers for a cohesive block of code dedicated to an application domain, a workflow, or a closely related set of capabilities
 describes how the application parts fit together.
root module
Every Angular app has at least one NgModule class, the root module, which is conventionally named AppModule and resides in a file named app.module.ts. You launch your app by bootstrapping the root NgModule.
NgModule decorator
@NgModule decorator identifies AppModule as an Angular module class (also called an NgModule class)
a function that takes a single metadata object, whose properties describe the module. The most important properties are as follows.
declarations: The components, directives, and pipes that belong to this NgModule.
exports: The subset of declarations that should be visible and usable in the component templates of other NgModules.
imports: Other modules whose exported classes are needed by component templates declared in this NgModule.
providers: Creators of services that this NgModule contributes to the global collection of services; they become accessible in all parts of the app. (You can also specify providers at the component level, which is often preferred.)
bootstrap: The main application view, called the root component, which hosts all other app views. Only the root NgModule should set the bootstrap property.
Component
A component and its template together define a view. 
A component controls a patch of screen called a view
define a component's application logic—what it does to support the view—inside a class. The class interacts with the view through an API of properties and methods.
referenced in HTML and what services it requires.
Component decorator
 @Component 
identifies the class immediately below it as a component class, and specifies its metadata. 
The metadata for a component tells Angular where to get the major building blocks that it needs to create and present the component and its view. In particular, it associates a template with the component, either directly with inline code, or by reference. Together, the component and its template describe a view.
@Component metadata configures, for example, how the component can be 
template syntax
alters the HTML based on your app's logic and the state of app and DOM data. Your template can use data binding to coordinate the app and DOM data, pipes to transform data before it is displayed, and directives to apply app logic to what gets displayed.
Directives
Angular templates are dynamic. When Angular renders them, it transforms the DOM according to the instructions given by directives. A directive is a class with a @Directive() decorator.
attribute (ngClass, ngStyle, custom)
Attribute directives alter the appearance or behavior of an existing element. In templates they look like regular HTML attributes, hence the name.
Add or remove several CSS classes simultaneously with ngClass.
Use NgStyle to set many inline styles simultaneously and dynamically, based on the state of the component.
structural (ngFor, ngIf, ngSwitch)
Structural directives alter layout by adding, removing, and replacing elements in the DOM. 
*ngFor is an iterative; it tells Angular to stamp out one <li> per hero in the heroes list.
*ngIf is a conditional; it includes the HeroDetail component only if a selected hero exists.
NgSwitch is like the JavaScript switch statement. It displays one element from among several possible elements, based on a switch condition. Angular puts only the selected element into the DOM.
NgSwitch is actually a set of three, cooperating directives: NgSwitch, NgSwitchCase, and NgSwitchDefault
Ngswitch is an attribute directive. Rather than touching the DOM directly, it changes the behavior of its companion directives.
NgSwitchCase and NgSwitchDefault are structural directives
Components
Is technically a directive
However, components are so distinctive and central to Angular applications that Angular defines the @Component() decorator, which extends the @Directive() decorator with template-oriented features.
Data Binding

Interpolation - {{value}}, uses double curly braces
Property binding - [property] = “value”, uses single set of square brackets
Event binding - (event) = “handler” , uses single set of parenthesis
Two-way binding  - [(ngmodel)] = “property”, uses single set of parenthesis inside square brackets
Like property binding and event binding together
NgModel:
Creates a FormControl instance from a domain model and binds it to a form control element.
Service
Service is a broad category encompassing any value, function, or feature that an app needs. A service is typically a class with a narrow, well-defined purpose. It should do something specific and do it well.
Angular distinguishes components from services to increase modularity and reusability. By separating a component's view-related functionality from other kinds of processing, you can make your component classes lean and efficient.
A component can delegate certain tasks to services, such as fetching data from the server, validating user input, or logging directly to the console. By defining such processing tasks in an injectable service class, you make those tasks available to any component. You can also make your app more adaptable by injecting different providers of the same kind of service, as appropriate in different circumstances.
Injectable decorator
Implements dependency injection in injecting services to components
To define a class as a service in Angular, use the @Injectable() decorator to provide the metadata that allows Angular to inject it into a component as a dependency. Similarly, use the @Injectable() decorator to indicate that a component or other class (such as another service, a pipe, or an NgModule) has a dependency.
The injector is the main mechanism. Angular creates an application-wide injector for you during the bootstrap process, and additional injectors as needed. You don't have to create injectors.
An injector creates dependencies, and maintains a container of dependency instances that it reuses if possible.
A provider is an object that tells an injector how to obtain or create a dependency.
For any dependency that you need in your app, you must register a provider with the app's injector, so that the injector can use the provider to create new instances. For a service, the provider is typically the service class itself.
When you provide the service at the root level, Angular creates a single, shared instance of the service and injects it into any class that asks for it. Registering the provider in the @Injectable() metadata also allows Angular to optimize an app by removing the service from the compiled app if it isn't used.
Routing
Router-outlet tag: used to provide a location where routed components will appear in view
routerLink property: Provide a link to a route
Configure all paths in app-routing-module, indicate path and component
HttpClient
Angular provides a way of making asynchronous requests with HttpClient Module
Built on top of AJAX, allows you to get to the API
A service used to send HTTP requests
Observable: an asynchronous stream of data which can be subscribed to, can be cancelled, can be resolved more than once (“subscribing” - can be subscribed to multiple times), from RxJS (Reactive Extensions for Javascript) 
Promise: cannot be cancelled, can only be resolved once, async request as well
Testing 
Jasmine
 behavior-driven development framework for testing JavaScript code that plays very well with Karma. 
Karma
the default test runner for applications created with the Angular CLI.
ng CLI
Angular CLI
Used to run commands on Angular such as building projects and running tests
Deployment
npm install
npx ng  build --prod
Deploy using pipeline in Azure