# Switch Local Git Repos to use SSH

When pushing changes to github, I'm continually promted for a username
and password, even though I'm fully configured to use SSH via git. The
underlying issue is that my original `git clone` used HTTPS.

To fix this, within `.git/config`, change the URL to denote SSH.

``` bash
url = https://github.com/rossim2i2/reponame
```

to

``` bash
url = git@github.com:rossim2i2/reponame
```

Save the file and you are good to go.

    #git #tips #ssh

