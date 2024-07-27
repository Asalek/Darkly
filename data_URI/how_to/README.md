
# Cookies weak increption

how i found the flag:

on the home page only the third image clickable, once clicked a page with header http://x.x.x.x/?page=media&src=nsa
shown, notice that src is there we might attack it using the URI to push a script 

1_ after a search the data URI format is : data:[<mediatype>][;base64],<data> 
2_ as we wanna to push a script to it we must encode it before
3_ encode <script>alert(1337)</script> to base 64 to get PHNjcmlwdD5hbGVydCgxMzM3KTwvc2NyaXB0Pg==
4_ replace the data with encoded script :
http://127.0.0.2/?page=media&src=data:text/html;base64,PHNjcmlwdD5hbGVydCgxMzM3KTwvc2NyaXB0Pg==
5_ enjoy the flag

## to resolve the patch

1_ Use a database rather than an identifier to load resources
2_ Hide header sensitive params

## Source
URI and URL :
* https://waytolearnx.com/2018/09/difference-entre-uri-et-url.html
Data URI :
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URLs