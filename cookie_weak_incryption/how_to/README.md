
# Cookies weak increption

how i found the flag:

open the website x.x.x.x and inspect page, open burpsuite and interupt the rquest
in cookies switch i am admin boolen to true with this  b326b5062b2f0e69046810717534cb09

b326b5062b2f0e69046810717534cb09 : true (incrypted with md5)

voila you'll get the flag

## to resolve the patch

1_ cookie must contains only users info
2_ store admin users in a seprated table and check admin privileges from it