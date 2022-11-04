# Managing Repositories:

## 1) Code base: 


## 2) Issues:


## 3) Projects:


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
