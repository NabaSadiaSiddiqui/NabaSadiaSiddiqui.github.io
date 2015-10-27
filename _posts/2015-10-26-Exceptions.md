---
layout: post
title: Checked exception vs. unchecked exception
---

According to an [Oracle](https://docs.oracle.com/javase/tutorial/essential/exceptions/) tutorial,
> An exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions.
 
Java uses exceptions as an error-management technique.  There are two kinds of exceptions in Java: checked exceptions and unchecked exceptions. This blog aims to cover the differences between them.
 
**Checked exceptions** represent events that fall outside the functional scope of a program. Example of such events includes invalid user input. All checked exceptions are a subclass of `Exception`. A method is required to handle all checked exceptions, either by passing it higher in the hierarchy or handling it some other way (e.g. logging the exception and terminating the program).
 
**Unchecked exceptions** represent events that are created by errors in program's logic and are not recoverable at run time. Unchecked exceptions subclass `RuntimeException`, which is itself a subclass of `Exception`. A method is not required to handle an unchecked exception.
 
Some of the [best practices](http://howtodoinjava.com/2013/04/04/java-exception-handling-best-practices/) around exception handling in Java include:

1. Never swallow the exception in `catch` block
2. Declare the specific checked exception that your method can throw
3. Do not catch the `Exception` class rather catch specific sub classes
4. Never catch `Throwable` class
5. Always correctly wrap the exceptions in custom exceptions so that stack trace is not lost
6. Either log the exception or throw it but never do the both
7. Never throw any exception from `finally` block
8. Always catch only those exceptions that you can actually handle
9. Don't use `printStackTrace()` statement or similar methods
10. Use finally blocks instead of catch blocks if you are not going to handle exception
11. Remember **Throw Early Catch Late** principle
12. Always clean up after handling the exception
13. Throw only relevant exception from a method
14. Never use exceptions for flow control in your program
15. Validate user input to catch adverse conditions very early in request processing
16. Always include all information about an exception in single log message
17. Pass all relevant information to exceptions to make them informative as much as possible
18. Always terminate the thread which it is interrupted
19. Use template methods for repeated `try-catch`
20. Document all exceptions in your application in javadoc
