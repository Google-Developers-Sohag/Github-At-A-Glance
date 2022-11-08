# Un-doing changes

### `$  git reset [--soft | --mixed [-N] | --hard | --merge | --keep] [-q] [<commit>]`

| `Soft Reset` | 
|-------------|
| Resets to a commit keeping the file changes stashed (false reset). |
```bash   
┌─[pavl-machine@pavl-machine]─[/]
└──╼ $cd /home/pavl-machine/Hello-World/ && cat ./README.md
# Hello-World

- This is repository represents a quick tutorial for Github-Training sessions.
- This is a test for our new feature
- Test 2
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
└──╼ $git reset --soft 762f43cb57e35a8f843638c34e3a03760dabf43b && cat ./README.md 
# Hello-World

- This is repository represents a quick tutorial for Github-Training sessions.
- This is a test for our new feature
- Test 2
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git log
commit 762f43cb57e35a8f843638c34e3a03760dabf43b (HEAD -> session-info)
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
└──╼ $

```
As you can see, only the data of the logs has changed by doing a soft reset, the file README.md hasn't changed !

| `Hard Reset` |
|--------------|
| Resets the file changes to a particular commit discarding everything including file changes (true reset). |
```bash   
┌─[pavl-machine@pavl-machine]─[/]
└──╼ $cd ./home/pavl-machine/Hello-World/ && cat ./README.md
# Hello-World

- This is repository represents a quick tutorial for Github-Training sessions.
- This is a test for our new feature
- Test 2
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
└──╼ $git reset --hard 762f43cb57e35a8f843638c34e3a03760dabf43b && cat ./README.md 
HEAD is now at 762f43c Merge pull request #1 from Arithmos-Algorithms/session-info
# Hello-World

This is repository represents a quick tutorial for Github-Training sessions.
This is a test for our new feature
┌─[pavl-machine@pavl-machine]─[~/Hello-World]
└──╼ $git log
commit 762f43cb57e35a8f843638c34e3a03760dabf43b (HEAD -> session-info)
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
└──╼ $git reset --hard cb193cbba1badbed23f94f98a24549c4d33acb62 && cat ./README.md
HEAD is now at cb193cb Update README.md
# Hello-World

- This is repository represents a quick tutorial for Github-Training sessions.
- This is a test for our new feature
- Test 2
```
As you can see, the hard reset, changes the core file changes in addition to the commit data, and reverting back the hard reset will return 
the files and the commits unchanged.
