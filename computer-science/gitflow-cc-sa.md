# Git workflow with conventional commits and semantic auto release

## The main concepts

At the core, the development model is greatly inspired by existing
models out there. The central repo holds two main branches with an
infinite lifetime:

- main
- develop

We consider **origin/main** to be the main branch where the
source code of HEAD always reflects a _production-ready_ state.

We consider **origin/develop** to be the main branch where the 
source code of HEAD always reflects a state with the latest
delivered development changes for the next release. Some would
call this the "integration branch".

- Direct push to **main** and **develop** branches is forbidden.
- Every push to **develop** branch will deploy to staging.
- Every push to main will create a new release and deploy to production.
- Merge requests of feature and hotfix branches ONLY into develop branch.

Before merging a MR into **develop** branch the CI should pass (merge button disabled untill it's done).

## Feature branch

- May branch off from: **develop**
- Must merge back into: **develop**
- Branch naming convention: **feat/CLICKUP-TASK-ID-short_describe**

### Creating of a feature branch

When starting work on a new feature, branch off from the develop branch.

```
$ git checkout -b feat/DE-xxx-short_name develop
Switched to a new branch "feat/DE-xxx-short_name"
```

### Merging a finished feature into develop

To merge feature branch into **develop** you should push your local branch
to origin and then create a MR into **develop**. This is done to user power
of CI and do all checks automatically before merging.

```
# Push to origin
git push -u origin feat/DE-xxx-short_name
```

When MR is created CI must run. In most cases it will have the following jobs _lint_ _test_ _build_.

- Merge button should be disabled until all checks pass.
- Merge button can also be disabled until MR gets two approves or it can be just an agreement in a team.

#### Squash or Merge or Rebase

##### Squash

Tracking how feature was developed is good thing, but only in the
ideal world where it includes just a few commits and every one is meaningful.

Feature branches are frequently considered as "fat" branches that contain a lot
of commit sthat make history unclean and unconcise, for example:

- feat: add new feture
- fix: something I forgot to do
- fix: and again
- chore: adopt review changes
- chore: adopt review changes 2
- chore: final commit, I promise

In this case no real need to see these commits in **develop** branch.
Squashing will combine all your commits into one.

To squash changes select "Squash and merge" option on MR merge button in github.

## Hotfix branch

- May branch off from: **develop**
- Must merge back into: **develop**
- Branch naming convention: **fix/CLICKUP-TASK-ID-short_describe**

When develop branch already has new features and a _fix_ is needed in production then:

- create a hotfix branch from **main**
- commit fix with commit message like `fix: what was fixed`
- create MR into main (after merging release process will be triggered)
- create MR from main into develop (CI will run on MR and after merge deployed to staging)
- delete hotfix branch

**NOTE:** merging a hotfix branch into develop and main should be done with _merge commit_.

##### Rebase

It's possible to rebase commits from feature (or fix) branch into develop if **ALL** of them are self-descriptive (have meaningful commit comment and are responsible for their purpose).

##### Merge

It's not allowed to merge feature/fix/whatever branch into develop so that git history will be clean and without merge commits.

## Release

In most cases release will be done in the following way:

- create MR from **develop** into **main**
- merge it with merge commit (NO squash and rebase)
- ci should pass
- new release created and deloyed to production

Sometimes release should be done in a few days with the _current_ state, but we do not want to block other developers from merging new features into **develop** branch. In this case we can borrow idea of a release branch from git flow.

- create new branch from **develop**
- now we can continue merging into develop branch
- when we want release the stuff we create a MR from this **release** branch into **main**
- then the flow as described above when merging develop into main

## Conventional commits

The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of. This convention dovetails with SemVer, by describing the features, fixes, and breaking changes made in commit messages.

More info here: https://www.conventionalcommits.org/en/v1.0.0/

## Semantic release

https://github.com/semantic-release/semantic-release

## Credits

This is an adoptation of [Git flow by Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)
with conventional commits and semantic release.

Based on https://gist.github.com/vtenq/7a93687108cb876f884c3ce75a8a8023