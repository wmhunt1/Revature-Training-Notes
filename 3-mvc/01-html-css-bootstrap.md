* What is HTML?
    * Stands for hyptertext markup language 
    * This defines the structure of the web
    *  What goes where 
    * Use tags to describe the elements of your webpage
* How is your webpage read by the browser?
    * 4 Steps
        1. Request - Client requests
        2. Response - server responds
        3. Build - browser builds
        4. Render
* HTML Version
    * We’ll be working with HTML5 
    * HTML5 is the living standard 
    * HTML has gone through some transformation through the years, at some point there was even an xhtml, which actually imposed errors on the HTML page 
    * The Web Hypertext Application Technology Working Group (WHATWG) is in charge of maintaining this living standard
* Semantic Elements
    * HTML5 introduced semantic elements
    *  These are elements that clearly describe their meaning in a human readable way 
    * Examples include: <header>, <article>, <footer>
* What is CSS?
    * Stands for Cascading Style Sheets
    *  Applies style in webpage using cascading algorithm 
        * Really fancy way of saying style is applied in layers 
    * Since html describes the structure of the webpage, css describes the style
* Ways to include CSS
    1. Inline  
        * uses style attributes of html tags
    2. Internal
        * uses style tag in head
    3. External
        * Uses seperate files
        * Referneced in head
        * Best practice
* How are styles applied
    * We apply styles using rules in CSS. 
    * Rules are a key value pair of what element property to style, and the style that should be applied.  
    * For example, the rule, color:yellow, changes the font color of the selected element to yellow. 
    * Selectors are used to group these rules together. 
    * Using selectors, we can define a set of style rules for a certain group of elements.
* Order in which styles are applied
    1. Importance
        * adding! means will always be applied
    2. Specificity 
        * order
        * inline
        * id
        * class/attr/psuedo class
        * element/psuedo element
    3. Source order
* Responsive Web Design
    * Designing pages so they render well on any window. 
    * And, if you're really good at CSS you can address these concerns by yourself. 
    * But why should you?