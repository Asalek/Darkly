# Overflow Patch

how i've found the flag:

in survey page choose one to vote for and select any number, intercept the request with burpsuite.
then increse the value and make more than 10. the server will overflow and crashed.

## how to resolve the patch :

1_ before runing any operation a type check must be first
2_ check the value in server side
3_ try except must be present to handke unexpected errors
