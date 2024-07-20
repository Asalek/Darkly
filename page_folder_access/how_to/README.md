# Folder page access LFI (Local file inclusion)

how i've found the patch

on the website go to x.x.x.x/?page=../../../../../../../etc/passwd

## how to resolve the patch

1_ deny user from accessing platform folders:
    - implement a route method