
# Url redirect

in url redirect the website doesn't protect users from bieng redirected into another website

1_ open x.x.x.x site and click on facebook or insta or twitter and interupt the request with burpsuite
2_  in the header request : GET /index.php?page=redirect&site=twitter HTTP/1.1 change twitter to whatever you wan't
3_ enjoy (^_^)

## how to resolve the patch

1_ the redirection must be done withing server side