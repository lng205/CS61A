# Notes

[textbook](http://composingprograms.com/)

## CH1

### Pure functions

Pure functions have the property that applying them has no effects beyond returning a value. Moreover, a pure function must always return the same value when called twice with the same arguments.

### Enviroments

Enviroments allow objects to share names without confusion.

The name of a function is repeated twice, once in the frame and again as part of the function itself.The name appearing in the function is called the intrinsic name. The parent frame of a function is where it's **defined**.

### Calling functions

As with any call expression, the interpreter evaluates the operator and operand expressions, and then applies the named function to the resulting arguments.

Applying a user-defined function introduces a second local frame, which is only accessible to that function. To apply a user-defined function to some arguments:

1. Bind the arguments to the names of the function's formal parameters in a new local frame.
2. Execute the body of the function in the environment that starts with this frame.

### Name Evaluation

A name evaluates to the value bound to that name in the earliest frame of the current environment in which that name is found.

### Higher-Order Functions

With higher-order functions, we begin to see a more powerful kind of abstraction: some functions express general methods of computation, independent of the particular functions they call.

### Golden Ratio

Golden Ratio is the ratio of fibonacci, which coule also be obtained by continue fraction: 

$$(1+x)^{-1}$$

plot y=x and the function above in the same graph, choose a positive x, draw a vertical line meeting the function, then draw a horizontal line meeting y=x. Repeat the last two steps. The result would converge to the crossing point, which is the golden ratio.

### Newton's Method

Newton's method is a powerful way to find zero points using improve-close iteration method. The starting point of the algorithm need to be small enough to converge.

### Curring

Converting a function that takes multiple arguments into a single-argument higher-order function.

    curry(f)(x)(y)=f(x,y)

### Lambda function

A lambda expression evaluates to a function that has a single return expression as its body.

        lambda            x            :          f(g(x))
    "A function that    takes x    and returns     f(g(x))"

### First class elements

Some of the "rights and privileges" of first-class elements are:

1. They may be bound to names.
2. They may be passed as arguments to functions.
3. They may be returned as the results of functions.
3. They may be included in data structures.

Python awards functions full first-class status, and the resulting gain in expressive power is enormous.

### Recursive

The sum of digits have same remainder mod 3:

$$10^k \equiv 1\mod 3$$

Iteration is a special case of recursion. 
