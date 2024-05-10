# Debugging

Debugging is crucial for identifying and resolving errors in code, ensuring that applications function correctly and reliably. It helps developers understand the root causes of issues, leading to improved code quality and better user experiences.

Below are some useful `console` methods to achieve that.

## Helpful Logs

Below are some helpful logs used in Javascript to display your data in the terminal or the console.

### General Debugging

*Use for checking data types or general debugging*

`console.log()`

console.log(): This is the most basic logging method. It prints the specified content to the console. It's useful for general-purpose logging and can be used to output variables, objects, messages, etc. It's often used for debugging purposes to inspect the state of variables or to track the flow of execution.

### Info

*Outputs helpful information, this is more for informative information rather that the traditional debugging `console.log()`*

`console.info()`

console.info(): Outputs an informational message to the console. It's useful for logging general information about the execution of your code. Unlike console.log(), which is often used for debugging, console.info() is typically used for informative messages that don't necessarily require immediate attention.

### Warn

*Use this if something is about to go wrong, but is not a critical failure.*

`console.warn()`

console.warn(): Similar to console.error(), console.warn() logs a warning message to the console. It's used to highlight potential issues or unexpected behavior in the code without necessarily indicating a critical error.

### Error

*Use this when a critical error has occured that is outside of the expected functionality of your code*

`console.error()`

console.error(): Outputs an error message to the console. It's useful for logging errors, warnings, or exceptional situations in your code. Unlike console.log(), console.error() typically formats the output differently, making it easier to distinguish errors from regular log messages.

### Displaying Data

*Useful for outputting arrays or objects into the terminal*

`console.table()`

console.table() is a useful logging method in JavaScript that allows you to display tabular data in a structured format within the browser's console. It's particularly handy for logging arrays of objects or arrays of arrays, as it presents the data in a visually appealing table format.

### Run Time

`console.time()`
`console.timeEnd()`

*Useful for checking the total execution time of the function in milliseconds.*
If you're worried about efficiency or checking runtime.

### Debug

*Output a debug message*

`console.debug()`

console.debug(): Outputs a debug message to the console. It's similar to console.log(), but it's specifically intended for debugging purposes. Some browsers may suppress console.debug() messages by default, so it's often used for more detailed debugging when needed.
