## Errors and exception handling

### Java

Java has an error and exception handling system by using a combination of the try and catch keywords. A try/catch block is placed around the code that might generate an exception. 

```Java
try {
// Protected code
}catch(ExceptionName e1) {
// Catch block
}
```

- The code that may try to execute is placed in the try block. 
- When an exception occurs, that exception occurred is handled by catch block associated with it. 
- Every try block should be immediately followed either by a catch block or finally block.

- A catch statement involves declaring the type of exception you are trying to catch. 
- If an exception occurs in protected code, the catch block (or blocks) that follows the try is checked. 
- If the type of exception that occurred is listed in a catch block, the exception is passed to the catch block much as an argument is passed into a method parameter.

