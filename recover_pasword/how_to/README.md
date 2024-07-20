# Patch of mailing

how i've fonud the patch :

on login page click on forgot password, then click on submit. intercept the request with burpsuite, you'll noticed a mail webmaster%40borntosec.com change it to you're instead.

## how to resolve the patch

1_ always ask user to enter their mail.
2_ check always if the mail exists in database.
3_ operations must done on server side always