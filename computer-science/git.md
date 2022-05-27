# Git and GitHub

## Common CMDs

`git config –-global user.name "<name>"` set git name

`git config –-global user.email "<email address>"` set git email

`git init <repository name .git>` start a new repository

`git clone <url>` clone an existing repo

`git add .` stage all files

`git commit -m "Message goes here."` commit and add message

`git rm file1.txt` remove from statging

`git reset –hard <commit>` discards all history and goes back to the specified commit

`git status` get git status

`git log` get git log

`git diff` get diff with previous

`git branch <branch name>` create branch

`git checkout <branch name>` switch from one branch to another

`git checkout -b <branch name>` create a new branch and switch to it

`git pull origin main` pull from origin master branch

`git push origin main` push to origin master branch

`git push origin <branch name>` push to branch

## How to contribute to open source

1. For a project
2. Clone the forked project
3. Create a branch for the edit
4. Push to your branch
5. Create the pull request on github
6. After that is approved and merged, delete branch and fork

## How to Sync Forked repo

1. Type `git remote -v` and press Enter. You'll see the current configured remote repository for your fork.

```
git remote -v
origin  <https://github.com/YOUR_USERNAME/YOUR_FORK.git> (fetch)
origin  <https://github.com/YOUR_USERNAME/YOUR_FORK.git> (push)
```

1. Type `git remote add upstream`, and then paste the URL you would copy from the original repository if you were to do a git clone. Press Enter. It will look like this:

```
git remote add upstream <https://github.com/zero-to-mastery/PROJECT_NAME.git>
```

1. To verify the new upstream repository you've specified for your fork, type `git remote -v` again. You should see the URL for your fork as origin, and the URL for the original repository as upstream.

```
git remote -v
origin    <https://github.com/YOUR_USERNAME/YOUR_FORK.git> (fetch)
origin    <https://github.com/YOUR_USERNAME/YOUR_FORK.git> (push)
upstream  <https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git> (fetch)
upstream  <https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git> (push)
```

Now, you can keep your fork synced with the upstream repository with a few Git commands.

One simple way is to do the below command from the master of your forked repository:

```
git pull upstream master
```

## Articles
- [Oh Shit, Git](https://ohshitgit.com) - Figuring out how to fix your "Git" mistakes
- [Oh My Git!](https://ohmygit.org/) - An open source game about learning Git!
- [How to ease your code review](https://medium.com/gogovan-technology/how-to-ease-your-code-review-2254baa867b6) - How to make ease the code review
- [Syncing a fork - GitHub Docs](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)
- [Top 20 Git Commands With Examples - DZone DevOps](https://dzone.com/articles/top-20-git-commands-with-examples)
- [Git Commands and Examples](http://www.yolinux.com/TUTORIALS/Git-commands.html)

## Videos

- [Traversy Media - Git & GitHub Crash Course For Beginners](https://www.youtube.com/watch?v=SWYqp7iY_Tc)
- [The Ultimate Git & GitHub Crash Course - Learn to Version Control for Beginners](https://www.youtube.com/watch?v=i76ts_0UryI)
- [GitLens Extension in Visual Studio Code](https://www.youtube.com/watch?v=C6wMNoe78oc)
- [5 Ways to DevOps-ify your App - Github Actions Tutorial](https://www.youtube.com/watch?v=eB0nUzAI7M8)
- [Git Forking & Fetch: How to Keep your Fork in Sync with an Upstream Repository](https://www.youtube.com/watch?v=deEYHVpE1c8)

## Tools
- [Git Explorer](https://gitexplorer.com) - Git Command Explorer
- [Learn Git Branching](https://learngitbranching.js.org) - Learn how to create branches with Git
- [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) - Git workflow that helps with continuous software development

## Other
- [Github Profile Makeover](https://www.youtube.com/watch?v=vblMsgrGjrw)
- [Conventional Commit](https://www.conventionalcommits.org/en/v1.0.0/)