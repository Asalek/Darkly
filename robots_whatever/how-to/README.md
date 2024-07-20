# Robots accessable

## how i've found the flag :

i've tried to get to sensitive files such as robots.txt, (Robots.txt: File declaring what should be excluded from indexing.) whith help of dirbuster (a tool that list all x.x.x.x/files)

the x.x.x.x/robots.txt shows me two files :
                                    Disallow: /whatever
                                    Disallow: /.hidden

1_ head to x.x.x.x/whatever and downlaod the htpasswd file listed on it.
2_ open file to find (root:437394baff5aa33daa618be47b75cb49) writen in it
3_ it seems like it's a md5 encryption, md5 decrypt website to decrypt it, 
4_ qwerty123@ founded


## sources

md5 decrypter :
*                https://hashes.com/en/decrypt/hash