# Setup git command line client side tool:

**Git**: is a command-line client-side api used to manipulate data between local (disk changes) and remote repositories (github remote repos).

## For windows: 

[Git-Executable-Binaries](https://git-scm.com/download/win)

## For Linux and Mac: 

- [Linux/Unix](https://git-scm.com/download/linux)
- [Mac](https://git-scm.com/download/mac)

## Official API Documentation:

[Git-Client-Side-API Documentation](https://git-scm.com/docs)

## Hands on git api:

- Clone the repository `Hello-World`, that you have created from [Introduction-to-github]() part using `git`.

![]()

`$ cd P:\Projects\ && git clone https://github.com/USER-NAME/Hello-World.git`

- Now let's create a branch to add a new feature.

- Checkout from the current branch [master] to a new branch [session-info].

`$ cd P:\Projects\Hello-World && git checkout master -b session-info`

- Now let's add some changes to our files, commit them and push to the branch `session-info`: 

`$ cd P:\Projects\Hello-World && git add ./README.md`
`$ cd P:\Projects\Hello-World && git commit -m 'README.md: Added session data'`
`$ cd P:\Projects\Hello-World && git push origin session-info`

```
Notes:
    # cd: change directory command, changes the working directory for the current terminal process.
    # &&: is the logical AND operator, it basically binds the return of both commands [the cd] and [the git].
    # Each command returns either 0 for success or 1 for failure, the return value is usually recorded in $? variable.
    # Example: 
 
    ┌─[pavl-machine@pavl-machine]─[~]
    └──╼ $cd /Projects
    bash: cd: /Projects: No such file or directory
    ┌─[✗]─[pavl-machine@pavl-machine]─[~]
    └──╼ $echo $?
    1
    ┌─[pavl-machine@pavl-machine]─[~]
    └──╼ $cd /home/
    ┌─[pavl-machine@pavl-machine]─[/home]
    └──╼ $echo $?
    0
    
    # Instead of using `$ cd P:\Projects\Hello-World && git push origin session-info`, you can change directory only one time, so a
    substitute for the above commands will be as follows: 
    
    $ cd P:\Projects\ && git clone https://github.com/USER-NAME/Hello-World.git
    $ cd P:\Projects\Hello-World
    $ echo 'New-Feature' >> README.md
    $ git add ./README.md
    $ git commit -m 'README.md: Added session data'
    $ git push origin session-info

```

- Now our new branch `session-info` which comes off the `master` branch is ahead of the master by one commit [README.md: Added session data'].

- You can view this analogy on github server-side user interface:
![]()

- Our new branch is ahead of the master, so, if you want to get the new feature from our new branch and keep the `master` up-to-date, we have to create a pull request.

- A `pull request` is a basically a request made by a github-user to merge some commits into the master branch.

- This is how to make a PR from your github repository: 
![]()

- These are the PR components, fill out your PR data here: 
![]()




