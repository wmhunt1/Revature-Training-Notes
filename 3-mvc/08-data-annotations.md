
* Data Annotations: Data Annotation validators enable you to perform validation simply by adding one or more attributes to a Model class property.
* Data Annotations – Overview
    * The DataAnnotations namespace provides a set of built-in validation attributes that are applied declaratively to a class or property. DataAnnotations also contains formatting attributes like DataType that help with formatting but don't provide validation.
* Annotations to Display and Edit
    * [Display()]
        * [Display(Name ="Film Genre")]  This gives the View the desired name for Display in the browser
    * [DataType()]
        * [DataType(DataType.Password)] Displays the types’ text as dots to obscure the actual content.
* Annotations for Validation
    * [Required] - The property is not allowed to be null
    * [Range(x,y)] - X is the minimum. Y is the maximum.
    * [StringLength(x)] - X is the maximum length of the property
    * [RegularExpression] - [RegularExpression(@"^[A-Z]+[a-zA-Z0-9""'\s-]*$")]
    * [MinLength(x)] - Minimum length is x. Also sets DB column size max.
    * [MaxLength(y)] - Maximum length is y. Also sets DB column size max
* 