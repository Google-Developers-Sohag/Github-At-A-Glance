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

![image](https://user-images.githubusercontent.com/60224159/199949223-5292c78a-f150-4317-be3a-37eab01e4149.png)

- Wikis represent a user-friendly documentation for your project or API.
- It has 2 sections, topics and contents.

## 5) Insights: 

![image](https://user-images.githubusercontent.com/60224159/199949613-c066a882-19c4-4a40-bddf-df4df7d6700c.png)

- Insights define the community outlines, including contributions, collaborators, contributions rule and licence.

## 6) Settings: 

- Defines the general repository settings (name, template png,...).
- Defines the environments, tags, branches, github-actions, collaborators and teams and moderators options.

## 7) Updating your local repository with the remote repository:

- If you have changed some data from the server-side interface, you should update your local repository on your machine, you have 2 options, 
either `rebasing` or `pulling` the changes.

- Rebasing V.S. Pulling 

| `Rebasing` | `Pulling` |
|------------|------------|
| Rebasing reapplies a series of commits on top of another commit without modifying the commit data. | Pulls the changes from a branch to another keeping the commits as they are |
| Usage: Redirecting the base of a branch divergency. | Usage: updating data with the new commits. |

Examples: 

```bash
$ git rebase master session-info # rebases (redirects the divergency of) the session-info on top of the last commit on the master branch
```
This the change: 

![image](https://user-images.githubusercontent.com/60224159/199960836-94af5797-b536-4eac-a2b8-c2eefe27f3ca.png) `--->` ![image](https://user-images.githubusercontent.com/60224159/199961344-23087826-cce8-4375-812b-ff7fd6669fe8.png)

Now the base of where the branch [sesssion-info] diverges is from the last commit `G` of the master branch.

```bash
$ git pull origin session-info # pulls the commits with the changes from the remote repository to the local repository
```
