# What is an `Interface`?

From rwxrob Go Programming conf-go video on 10/03/2021.

An interface says "this thing can do this operation."

Here is the name of the operation. Here are the arguments it will take.
Here is what it will return.

In addition, documentation is included above it for anyone who is going
to implement the operation with a method (the contract).

Example:
Walk would be the operation
Move left leg, move right leg, etc... would be the method(s)

Many people call operations, methods, which is incorrect.

*A very general description of the expectation for anything that
implements a method that fulfils the interfaces operation.*

Interfaces allow you to pass a "thing" and strictly define it in your
arguments, as long as it fulfils the stated interface.

Due to this, most interfaces are tiny - one or two operations
(methods?).

Instead of saying this "is" a thing, you are saying, this "has" a
certain capability.

Tags:

    #golang #interface #method #operation
