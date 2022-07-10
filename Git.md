#### ERROR : 
> npm ERR! fatal: unable to connect to github.com: npm ERR! github.com[0: 13.114.40.48]: errno=Connection timed out


##### Solution :

> `git config --global url.https://github.com/.insteadOf git://github.com/`