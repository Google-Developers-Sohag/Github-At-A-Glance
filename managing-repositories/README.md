# Managing Repositories:

## 1) Code base: 

![image](https://user-images.githubusercontent.com/60224159/199931457-3427cdad-54df-45e8-98a1-bb7a766b497c.png)

- Changing the branch, will switch the code base and the commits history.
- Each commit has title, author/s, code changes, hashcode, parent hashcode and date of modifications.

## 2) Issues:

![image](https://user-images.githubusercontent.com/60224159/199933603-3e15ff97-b4fc-475d-a01d-1c4850c05800.png)

1) Issue title.
2) Issue description.
3) Issue community insights.

- Issues represent bugs, feature requests, defects and many more...
- Issues is a good way to keep track of the current project bugs and feature list.
- You can also link a PR to an issue, the issue will be closed automatically after merging the PR.

## 3) Projects:

![image](https://user-images.githubusercontent.com/60224159/199934338-62a6e3f0-b097-4b8e-a0ba-6749642e7d0c.png)

- Projects is a good way to organize your projects in the form of todo-lists and notes and link them to your issues and PRs.
- This strategy deals more with the project management aspects of software engineering.

## 4) Wiki: 

## 5) Insights: 

## 6) Settings: 

## 7) Updating your local repository with the remote repository:

- If you have changed some data from the server-side interface, you should update your local repository on your machine, you have 2 options, 
either `rebasing` or `pulling` the changes.

- Rebasing V.S. Pulling 

| `Rebasing` | `Pulling` |
|------------|------------|
| Rebasing reapplies a series of commits on top of another commit without modifying the commit data. | Pulls the changes from a branch to another keeping the commits as they are |
| Usage: updating data while ignoring the commits to resolve conflicting commits. | Usage: updating data with the new commits. |

Examples: 

```bash
$ git rebase session-info master # rebases the master on top of the last commit on the session-info branch
```
```bash
$ git pull origin session-info # pulls the commits with the changes from the remote repository to the local repository
```
