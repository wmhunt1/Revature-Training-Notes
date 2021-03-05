* Unit Testing
    * Testing small units of your code. 
    * Helpful when you wanna make sure everything is working perfectly (without repeating some actions to get there). 
    * Also helpful in pinpointing where the code is going wrong. 
    * The unit testing framework we’ll be using is Xunit
* Parts of a unit test
    * Arrange
        * This is any setup necessary to prepare for the behavior to test. You assume the thing you wanna test works.
    * Act
        * You do the thing you wanna test. You usually name the method after the thing you wanna test.
    * Asset
        * Verify the behavior was as expected, sometimes on the same step as ACT. 
* Test-Driven Development
    * Add a Test
    * Run the tests
    * Make changes
    * Run the tests