
# Add wrong file as image

how i found the flag:

on home page click on add image, choose any file then click on upload,
interupt the request with burpsuite, and change the file Content-Type to image/jpeg or image/jpg.

why we choose image/jpeg or image/jpg but not any other format, cause of jpg and jpeg images can be executed and rendered on server making it the best choice to inject a script in it

## Usage/Examples

to resolve the patch :

1_ the website must deny users from uploading other formats
2_ verify only content-type
3_ check image size
