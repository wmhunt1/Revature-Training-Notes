* Application Monitoring
    * Highlighting certain events that come up during the runtime of your program
        * Highlighting events in the form of pausing program execution or recording its occurrence
    * Useful in finding points of failure, i.e, debugging
* Breakpoints
    * During development, you can add breakpoints to certain lines of your code
    * When you do a debug run, the program pauses its execution when it hits a breakpoint
    * Upon hitting a breakpoint, you can: 
        * Check the values of any variables in scope
        * Continue to the next breakpoint
        * Step over a function that is called
        * Step into a function that is called
        * Step out into the original line that called the function
* Logging
    * Practice wherein certain events during a program runtime is recorded
    * Events that warrant a record: 
        * Errors
        * Business logic events
            * Logging into the system
        * Transcations
* Logging Levels
    * Verbose
    * Debug
    * Information
    * Warning
    * Error
    * Fatal
* Where logs are?
    * Files
    * DB
    * Console
* Tracing
    * Confused with logging since they use similar software
    * Used to track a user’s interaction with the system
    * Unlike logging that shows the events that occur during runtime, tracing is highly involved in debugging and would include information such as which functions were called and what parameters were provided during the time the user interacted with the program.
    * You would go through the same steps as the user to find where the bug occurs
