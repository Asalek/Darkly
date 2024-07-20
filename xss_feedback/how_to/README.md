# Cross Site Scripting (XSS)

HOW I'VE FOUND THE FLAG

simply just add any script as comment and look at it if the page displayed and empty comments means the script got executed. for that we use the xss attack.

- put script in name and keep the comments empty or fill it with any thing

## how to resolve the patch : 

1_  In an HTML context, you should convert non-whitelisted values into HTML entities:

    < converts to: &lt;
    > converts to: &gt;
2_  Validating that input contains only an expected set of characters. 