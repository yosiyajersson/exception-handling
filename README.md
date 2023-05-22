# exception-handling

## 1.What is exception handling in java ?

Exception handling in Java is a mechanism that allows you to handle errors and exceptional conditions that may occur during the execution of a program. Java provides a robust exception handling framework that enables you to catch and handle exceptions, ensuring that your program can gracefully recover from unexpected situations.

When an exception occurs in Java, it disrupts the normal flow of the program and transfers control to a special block of code known as an exception handler. The exception handler is responsible for handling the exception and taking appropriate actions, such as logging the error, displaying an error message, or recovering from the exceptional condition.

The basic syntax for exception handling in Java consists of three main blocks:

Try Block: The code that may throw an exception is enclosed within a try block. If an exception occurs within the try block, it is immediately caught and passed to the appropriate catch block.

Catch Block: This block follows the try block and is used to catch and handle specific types of exceptions. Each catch block specifies the type of exception it can handle. If an exception of that type occurs, the catch block is executed.

Finally Block (optional): This block is used to specify code that should be executed regardless of whether an exception occurred or not. It is typically used for cleanup tasks, such as releasing resources (closing files, database connections, etc.) that were opened in the try block.

Here's an example that demonstrates exception handling in Java:

    try {
        // Code that may throw an exception
        int result = divide(10, 0);
        System.out.println("Result: " + result);
    } catch (ArithmeticException e) {
        // Exception handler for ArithmeticException
        System.err.println("Error: Division by zero");
    } finally {
        // Cleanup code
        System.out.println("Cleanup");
    }

    // Method that throws an exception
    public static int divide(int numerator, int denominator) {
        return numerator / denominator;
    }

