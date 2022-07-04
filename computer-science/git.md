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

# Conventions

## Git & Code Reviews
We know how much consistency within the codebase is important; the same philosophy must also be respected in the commit messages and MRs we create, so we try to follow these simple rules:

### Commit
For commit messages we use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). It is also possible to set a template for commit messages. To set it up it is recommended to follow this [guide](https://dev.to/timmybytes/keeping-git-commit-messages-consistent-with-a-custom-template-1jkm). To force the use of Conventional Commits within projects we could think of using [commitlint](https://github.com/conventional-changelog/commitlint).

### Branch
For the branching system we follow the famous [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) workflow

### Issues
It is necessary to correctly draft the issues in order to be able to identify them quickly and intervene on what is a priority.

#### Structure of an Issue

_Title of the Issue_
It is important that the title of the issue is clear and concise. A title that can quickly make people understand what the issue is about.

_Component_
It is essential to refer to the component to which the issue is logically related by means of the labels, in order to allow a quick identification of the topic.

Tags can be, for example, identified as:

* Platform - Generic on the platform
* Layout - Layout changes, UX tips, etc ...
* API - Communication problems with the API, Payload variations, etc ...

_Description_
Carefully draw up the description of the issue in order to allow other users to understand it as well.

_Assignment_
If the editor of the issue is not immediately clear which resource is useful for resolving the issue, the assignment can be made at a later time.

_Type and Priority_
It is necessary to correctly indicate the type, by means of the labels, between:
* Bug - Used to identify a platform bug
* Enhancement - Improvement of features already present on the platform
* Proposal - New feature to be screened (which will vary in task if accepted)
* Task - Anything that does not fit into the previous types
It is also essential to define the priority of the issue in order to define the resolution order of the issues themselves.

_Attachments, Comments, etc ..._
Everything that makes the issue complete must be drafted in the best possible way.
It is useful to remember that it is possible to link a member of the team in the comments by means of the @.

_Status_
The status of the issue must always be kept up to date.
The issues are created as a backlog on the board, and once evaluated they are moved in progress to then be taken over.
The subsequent status of the issues will subsequently be indicated according to the outcome of the resolution.

It is useful to remember what is indicated in the link for the automatic resolution of issues:
https://docs.gitlab.com/ee/user/project/issues/issues_functionalities.html#18-new-merge-request


### Merge Request
For each branch, let's get used to creating an MR so as to allow both a review of the code and the ability to link the Merge Request within Clickup.

Even in the case of MR we can follow some simple guidelines.
In the title of the MR we indicate whether it is a feature, bugfix or a refactor, while in the description we can use a template to briefly explain what the MR contains. The template I thought of is the following:

What does this change?
`<Explain what the MR contains and what changes have been made>`

Why is this change important?
`<Explain why we made the code changes and the value it carries>`

How can I test it?
`<Explain the steps to take to test the feature or fix you made>`

To keep the tree of commits and branches clean, before merging the MR, it is recommended to flag the two fields: Delete branch and Squash commit.
Once you have created the MR, enter yourself (ie the author of the MR) as Assignee, while as Reviewers specify the users who must review the code.

## GitFlow + Conventional Commits + Semantic Autorelease

[Gitflow+CC+SA](./gitflow-cc-sa.md)