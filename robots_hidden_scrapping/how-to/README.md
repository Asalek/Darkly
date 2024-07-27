# Robots File Accessed

## how i've found the flag

1_ after getting the page from robots.txt, go to x.x.x.x/.hidden
2_ notice too many folders no problem use this command :
* wget -r -e robots=off --no-parent http://x.x.x.x/.hidden/
the command will downlaod all folders
3_ look for a flag text inside thies folders with this command :
* grep -r "flag" ./path/
path/to/hidden : represent the folder that contains all the folder you downloaded with wget
4_ enjoy the flag (^_^)
