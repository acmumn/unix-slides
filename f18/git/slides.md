# Unix Class 2: Git
## By ACM UMN

---

### SSH into CSELabs

<img src="https://imgur.com/DQFGvXn.png"></img>

-----

```
ssh X500@csel-khROOM-NUM.cselabs.umn.edu

X500 = Your Internet ID
ROOM = 1250, 4240, 4250
NUM = 01 .. 20
```

-----

Then go get pizza!

---

# Log into github.umn.edu

---

## Fork This

https://github.umn.edu/acmumn/unix-f18-lesson-2

---

# Git Basics
## `clone`

`git clone` makes a clone of a remote repo.
Clone the repo you forked.

---

# Git Basics

Edit `main.c` to instead print `"Goodbye, world!"`.

---

![](https://git-scm.com/book/en/v2/images/areas.png)

---

# Git Basics
## `add` / `status`

To move changes from the **working directory** to the **staging area**, use `git add main.c`.
Alternatively, you can add the entire current directory with `git add .`.

Run `git status` to get the status of the repo.

---

# Git Basics
## `diff`

`git diff` will show you the differences between the **working directory** and **staging area**.

NOTE: Mention `git diff {ref}`, and `HEAD` as a ref.

---

# Git Basics
## `commit`

`git commit -m 'message'` will commit the **staging area** to a new **commit**.

NOTE: Pause for everybody who just got stuck in `vim`.
NOTE: Mention that commit hashes work as refs.

---

# Git Basics
## `pull` / `push`

`git pull` and `git push` allow you to copy commits from your **repo** to a **remote**.

---

# Git Theory
## Areas

 - **Working Directory**
 - **Staging Area**
 - **Repo**
 - **Remotes**

---

# Git Theory
## `.gitignore`

```
.*
!.gitignore

*.o
tmp/
/foo
```

---

# Git Theory
## The Commit Graph

---

# Git Theory
## Merging

---

## `checkout`

 - Switch to a different ref
   - `git checkout {REF}`
 - Delete uncommitted changes
   - `git checkout {REF} {FILE}`

---

## `diff`

Show a diff of changes.

`git diff`

`git diff {REF}`

---

## `reset`

`git reset main.c`

---

## `revert`

`git revert {REF}`

Create a *new commit* that undoes all of the previous commit's changes.

---

# Branch Model
## List Branches/Tags

`git branch`

`git branch -a`

`git tag`

---

# Branch Model
## Deleting Branches

`git branch -d {BRANCH}`

---

# Branch Model
## Switching Branches

`git checkout {BRANCH}`

---

# Branch Model
## Create a New Branch

`git checkout -b {BRANCH}`

---

# Branch Model
## Merge

`git merge {BRANCH}`

---

# Branch Model
## Rebasing

`git rebase {BRANCH}`

---

# Branch Model
## Creating Tags

`git tag`

---

 - Public GitHub
   - Educational Plan
 - Issues
 - PRs
 - Repos
 - Pages

---

If you want to know more advanced things:

 - `bisect`
 - `cherry-pick`
 - `submodule`
