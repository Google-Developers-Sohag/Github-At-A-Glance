# Setup git command line client side tool:

**Git**: is a command-line client-side api used to manipulate data between local (disk changes) and remote repositories (github remote repos).

## For windows: 

[Git-Executable-Binaries](https://git-scm.com/download/win)

## For Linux and Mac: 

- [Linux/Unix](https://git-scm.com/download/linux)
- [Mac](https://git-scm.com/download/mac)

## Official API Documentation:

[Git-Client-Side-API Documentation](https://git-scm.com/docs)

## Create an access token:

![image](https://user-images.githubusercontent.com/60224159/199989374-36693731-959a-473d-8c5d-3ffb589d041d.png)

Access tokens: replaces your passowrd for specific operations defined by some security permissions.

## Hands on git api:

#### `$ git <command> [<options>, <args>]`

- Clone the repository `Hello-World`, that you have created from [Introduction-to-github]() part using `git`.

![image](https://user-images.githubusercontent.com/60224159/199841859-7b9b930a-9c72-4e23-bed5-9ea03c497de4.png)

```bash
$ cd P:\Projects\ && git clone https://github.com/USER-NAME/Hello-World.git
```
- Now let's create a branch to add a new feature.

- Checkout from the current branch [master] to a new branch [session-info].

```bash
$ git checkout master -b session-info
```

- Now let's add some changes to our files:

```bash
$ echo 'This is a test for our new feature' >> README.md
$ git diff
diff --git a/README.md b/README.md
index 2b22fb6..056049e 100644
--- a/README.md
+++ b/README.md
@@ -1,3 +1,4 @@
 # Hello-World
 
 This is repository represents a quick tutorial for Github-Training sessions.
+This is a test for our new feature
```

- You can visualize your changes to the branch base files before commiting using the `diff` git command, it finds the difference between the current base code and your new code.

- Now, let's add the changes, commit them and push to the branch `session-info`: 
```bash
$ git add ./README.md
$ git commit -m 'README.md: Added session data'
$ git push origin session-info
```

```bash
Notes:
    - cd: change directory command, changes the working directory for the current terminal process.
    - &&: is the logical AND operator, it basically binds the return of both commands [the cd] and [the git].
    - Each command returns either 0 for success or 1 for failure, the return value is usually recorded in $? variable.
    - Example: 
 
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

```

- In order to visualize the commit logs for this branch, use the `git log` command: 
```bash
$ git log
commit ee27510b8ab1997d187bdec491b4c9b666bb7b54 (HEAD -> session-info)
Author: pavl_g <scrappers.tm@gmail.com>
Date:   Fri Nov 4 00:19:45 2022 +0200

    README.md: Added session data

commit 40cd1f88bde87179aa47c0588f62a14749bcab92 (origin/master, origin/HEAD, master)
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Thu Nov 3 14:27:51 2022 +0200

    README.md: added more info

commit 010843fdbb8b20ae83498763ce59cc01c6297eb6
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Thu Nov 3 14:16:21 2022 +0200

    Initial commit
```

- Now our new branch `session-info` which comes off the `master` branch is ahead of the master by one commit [README.md: Added session data'].

- You can view this analogy on github server-side user interface:

![image](https://user-images.githubusercontent.com/60224159/199846078-b3d03586-5289-49db-8076-ce5d07dbb4b9.png)

- Our new branch is ahead of the master, so, if you want to get the new feature from our new branch and keep the `master` up-to-date, we have to create a pull request.

- A `pull request` is a basically a request made by a github-user to merge some commits into the master branch.

- This is how to make a PR from your github repository: 

![image](https://user-images.githubusercontent.com/60224159/199846155-b5199d02-a9df-42db-b71c-3f2c2c9ad193.png)

- These are the PR components, fill out your PR data here: 

![image](https://user-images.githubusercontent.com/60224159/199846386-23b152b0-2faa-44f9-a660-5a812ac2aace.png)

1) PR branches redirection, this basically redirects your changes to a specific branch.
2) The PR data, the title and the description.
3) The PR community insights (reviewers, linked issues, flags, milestones and projects).
4) The PR commits with the proposed changes.

![image](https://user-images.githubusercontent.com/60224159/199846953-478fbeef-2971-4ea1-9c47-c9c473e1adb1.png)

- Merge this PR into the master: 

![image](https://user-images.githubusercontent.com/60224159/199855330-63234d9e-5b76-40c8-8737-a495044a570a.png)


