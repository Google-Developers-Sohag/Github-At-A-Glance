# Introduction to Github

## Prologue:

**Version Control**: is a platform that manages projects' features, releases, archives and controls the project versioning in a user-friendly and interactive way.

**Github**: is a version control platform designed to help organizations, open source projects, small teams and even independent developers
to carry out thier projects in a clean organized strategy and develop environments to manipulate projects releases and documentation.

Github is composed of organizations and github accounts.

**Organizations** and **github-accounts** have **repositories**, **projects**, **packages**, **members** and **teams** (organizations only).

An organization is considered a github account with special credentials related to the original author.

## Github Repository:

A github repository is composed of some `branches`.

Think of a repository as a tree.

### Tree V.S. Git-Repo branches

A tree has roots, a stem, branches and leaves.

A github repo has a `remote-url`, `master` branch and other descendant branch coming out of the master branch, each repository branch holds some `commits` (which represent the changes to the files).

The main repository branch is called the `master` branch and it holds the base code for the repository.

Each branch has a some `commits`, which represent the changes to the code from the master branch and those can synonmous to the new fearues
in the world of agile development.

A `pull request`: is basically a request made by a github-user to pull the code or file changes (represented by commits) from a branch to another (usually the master).

A pull request must be reviewed by the team members or the project owners before merging into the master branch.

A `develop` branch is a common use case for this.

| `Github Repositores have a tree-like paradigm` |
|-------------------------------------------|
| ![](https://github.com/Google-Developers-Sohag/Github-Training-Course/blob/github-intro/introduction-to-github/git-repos.png) |

## Create an empty repository on git:

- From your github acc or organization: 

| `Create new repo` | `Fill your repo data and initialize with a README file` |
|-------------------|---------------------------------------------------------|
| ![image](https://user-images.githubusercontent.com/60224159/199716852-34a17f73-3079-480c-aa6d-362de480531f.png) | ![image](https://user-images.githubusercontent.com/60224159/199718348-2bf2eac6-22c1-4d75-b935-bddb8aae0b77.png) | 

| `Preview` |
|-----------|
| ![image](https://user-images.githubusercontent.com/60224159/199719220-0785c661-4e6e-4d39-a58f-e8a85ca3212b.png) |

## Change some data and commit your changes: 
| `Edit README` | `Commit changes to the master` | 
|---------------|--------------------------------|
| ![image](https://user-images.githubusercontent.com/60224159/199719638-2552cd6f-1d1c-4912-b2c6-c923515b6c8e.png) | ![image](https://user-images.githubusercontent.com/60224159/199719999-8aba0053-6932-48f8-9ef1-15c7f2f0d018.png) |

## Review code changes on the `[master]` branch:

| `Commits history for this branch` | `Review Code changes` |
|----------------------------------|------------------------|
| ![image](https://user-images.githubusercontent.com/60224159/199720479-7b31412e-40ea-4f6c-a715-507f1949628f.png) | ![image](https://user-images.githubusercontent.com/60224159/199720613-017bff6e-2b31-420e-b967-8f63776b2e47.png) | 

| `Code changes` | 
|----------------|
| ![image](https://user-images.githubusercontent.com/60224159/199720964-d128ec66-c1e1-4655-8cd7-f06f0ffde5bb.png) |

## Learn repository parts: 

Each repository has some tabs: 
- Code tab: holds the current branch code base.
- Issues tab: holds the project issues opened by other developers or you.
- Pull requests tab: holds the commits pull requests from a branch to another.
- Actions tab: holds github actions for DevOps.
- Projects tab: holds the project outline and tasks created by you.
- Wiki tab: holds the project wikipedia created by you.
- Security tab: not so relevant for now.
- Insights tab: holds the community data including statistics of contributions, contribution rules and project licence.
- Settings tab.

![image](https://user-images.githubusercontent.com/60224159/199722000-32ad209d-feae-41a6-a7d9-05f340ffc5a9.png)

Each repository has some branches, this is how to visualize branches: 

![image](https://user-images.githubusercontent.com/60224159/199722357-ea39c362-1e7a-472b-906f-280e32ff26fa.png)



