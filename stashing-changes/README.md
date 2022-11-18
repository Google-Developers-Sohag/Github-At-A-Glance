# Stashing changes: 

Git-Stashing: is about stashing the changes in a dirty working directory away to work on them later before switching to another branch.

Use `git stash` when you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the `HEAD` commit

## Syntax:
```bash
$ git stash [push-pop] -m [<message>]
```
## Example: 
```bash
┌─[pavl-machine@pavl-machine]─[~]
└──╼ $cd /home/pavl-machine/Hello-World/ && echo "Test Stashing" >> README.md
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git status
On branch session-info
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git log
commit cb193cbba1badbed23f94f98a24549c4d33acb62 (HEAD -> session-info, origin/session-info, origin/master, origin/HEAD, master)
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Fri Nov 4 13:52:54 2022 +0200

    Update README.md

commit bc343beaf33d5ae9051b2eab60902b38318057e9
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Fri Nov 4 13:07:54 2022 +0200

    Update README.md

commit 762f43cb57e35a8f843638c34e3a03760dabf43b
Merge: 40cd1f8 ee27510
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Fri Nov 4 09:18:21 2022 +0200

    Merge pull request #1 from Arithmos-Algorithms/session-info
    
    README.md: Added session data

commit ee27510b8ab1997d187bdec491b4c9b666bb7b54
Author: pavl_g <scrappers.tm@gmail.com>
Date:   Fri Nov 4 00:19:45 2022 +0200

    README.md: Added session data

commit 40cd1f88bde87179aa47c0588f62a14749bcab92
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Thu Nov 3 14:27:51 2022 +0200

    README.md: added more info

commit 010843fdbb8b20ae83498763ce59cc01c6297eb6
Author: Scrappers Team <60224159+Scrappers-glitch@users.noreply.github.com>
Date:   Thu Nov 3 14:16:21 2022 +0200

    Initial commit
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git stash push -m 'README.md: test stashing'
Saved working directory and index state On session-info: README.md: test stashing
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git stash list 
stash@{0}: On session-info: README.md: test stashing
stash@{1}: WIP on session-info: cb193cb Update README.md
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $cat README.md 
# Hello-World

- This is repository represents a quick tutorial for Github-Training sessions.
- This is a test for our new feature
- Test 2
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git stash pop stash@{
stash@{0}   stash@{1}   
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git stash pop stash@{0}
On branch session-info
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{0} (8a851b2721f2515970bf937857a348abca2b69e1)
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $cat README.md 
# Hello-World

- This is repository represents a quick tutorial for Github-Training sessions.
- This is a test for our new feature
- Test 2
- Test 3
Test Stashing
```
