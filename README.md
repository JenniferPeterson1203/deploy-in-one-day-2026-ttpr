---
tags: deploy, team, git, pull request
languages: html, css
resources:
---

# Deploy on Day One

## Contents

| Section                                  |
| ---------------------------------------- |
| [History](#history)                      |
| [What You'll Build](#what-youll-build)   |
| [Quickstart](#quickstart)                |
| [Assignment](#assignment)                |
| [Choose Your Path](#choose-your-path)    |
| [Requirements](#requirements)            |
| [File Structure](#structure)             |
| [Getting Started](#getting-started)      |
| [Next Steps](#next-steps)                |
| [Final Steps](#final-steps)              |
| [Resources](#resources)                  |
| [Issues](#issues)                        |

## History

Welcome to TTPR! Every semester, a student index page is created. It looks something like [this](https://hessvacio.com/). Links from this page go to individual profiles, which look like [this](https://hessvacio.com/pages/museummultiverse.html).

## What You'll Build

**One tile**, on the class index page (this repo's `index.html`), for the student you're paired with. Clicking the tile takes you either to:

- a new in-repo profile page that you wrote (**Path A**), **or**
- the student's deployed portfolio site from the [`html-student-portfolio`](https://github.com/ttpr-lgcc/html-student-portfolio) lab (**Path B**).

That's the entire deliverable. To see what the finished thing looks like, open `index.html` in a browser **right now** and look at the existing "Hessvacio Hassan" tile. By the end of this lab your tile should sit next to it.

> **Tip:** to open it, find `index.html` in Finder/File Explorer, right-click → Open With → your browser. No server, no build step.

## Quickstart

The whole flow, in 7 steps. Each one has a longer section below — but skim this first so you can see the whole arc before you start.

1. **Fork** this repo. *One person per table* clicks the Fork button on GitHub and shares the new fork's URL with the table.
2. Everyone at the table **clones the fork** (not the original) to their laptop.
3. Each person `git checkout -b <their-student-name>` to make a **branch** named after the student they're profiling (e.g. `zoe-perez`). **Never work on `main`/`master`.**
4. **Pick a path** ([A or B](#choose-your-path)) and add the matching files: an HTML page + 3 pictures (Path A), or just 1 index picture (Path B).
5. **Edit `index.html`** — duplicate the existing student `<li class="home-blog-post">` block and fill in your student's info.
6. `git add` → `git commit` → `git push` your branch. Then your table picks **one branch** and merges everyone else's branches into it (resolving conflicts in `index.html`).
7. Open a **pull request** from that combined branch back to the original repo.

If at any point you're not sure where you are in those 7 steps, come back here.

## Assignment

Your assignment is to create a student profile for someone sitting at your table. By the end of this project, every student should have a profile for themselves that was created by someone else and every student should have created a profile for someone else. If you're sitting at a table of four, it might be easiest to pair up. If you're sitting at a table of three, it might be easiest to create the profile of the student clockwise to you. If you're sitting at a...well you get the picture.

Now if you're anything like me, you might be freaking out and wondering, "Am I making a webapp?!?!" The answer is no. You're just working with HTML and file structures. You don't need to know Rails, JavaScript, or even Ruby for this project. No need to freak out. Calm down! Seriously, you're making the rest of us nervous!!!

You'll have about three hours to complete the first section of this lab. Use that time to get to know your table, get familiar with git workflows, and re-familiarizing yourself with HTML. If you feel stuck, ask any instructor for help. **Keep in mind everyone in your table will be pushing to the same repository.** Think about using a workflow with your teammates that will minimize conflicts.

## Choose Your Path

There are **two ways** to get your assigned student onto the index page. Pick whichever fits where you are in the curriculum — both end with the student's tile on `index.html` linking somewhere meaningful.

### Path A — Build the profile page in this repo

This is the traditional flow described below. You'll add an HTML file to `students/`, drop pictures into `img/students/`, and the tile on `index.html` links to your new in-repo page (e.g. `students/zoe_perez.html`). Use this path if your student doesn't have a portfolio of their own yet.

### Path B — Link to their deployed portfolio

If your student has already worked through the [`ttpr-lgcc/html-student-portfolio`](https://github.com/ttpr-lgcc/html-student-portfolio) lab, they can deploy that portfolio to GitHub Pages and you link to it directly from this index. No new file in `students/` required.

The rough shape of Path B (you'll have to figure out the exact steps — that's part of the challenge):

1. Make sure your student's fork of `ttpr-lgcc/html-student-portfolio` is deployed via GitHub Pages (repo **Settings → Pages**, source: their default branch). The published URL will look like `https://<their-github-username>.github.io/html-student-portfolio/`.
2. Visit that URL in a browser and confirm it loads.
3. Drop their index/profile picture into `img/students/` like in Path A.
4. In this repo's `index.html`, duplicate the existing student `<li class="home-blog-post">` block, but point both `<a href>` attributes at the deployed portfolio URL instead of `students/<name>.html`.

Either path should result in a working clickable tile on `index.html`.

## Requirements

Please collect the following content from your assigned student for their profile. This content doesn't have to be finalized, but you need something. They'll be using this content as the project evolves for their resume and other profiles online.

- Name
- Github Username
- Blog Url (if they don't already have a blog it will be their-github-username.github.io)
- Tagline
- Profile Picture (something normal, a headshot, of a good reusable size that can be easily cropped)
- Background Picture
- Treehouse Account
- CoderWall Account
- CodeSchool Account
- Favorite Websites
- Previous Work Experience
- Short Bio
- Twitter URL
- LinkedIn URL
- Education

## Structure

The structure of this project looks something like this:

```text
├── README.md
├── css
│   ├── css style sheets
│   └── fonts
│       └── font files
├── img
│   ├── lots of images here
│   └── students
│       ├── student_name_background.jpg
│       ├── student_name_index.jpg
│       └── student_name_profile.jpg
├── index.html
├── js
│   └── javascipt files
└── students
    └── student_name.html
```

### Files you will need to alter:

- You'll always alter `index.html` to add a tile for your student.

### Files you will need to add:

**For Path A (in-repo profile):**

- Add three pictures to the `img/students` folder (they can be jpg or png files):
  - A background picture
  - A picture for the index page
  - A picture for the profile page
- Add one HTML file to the `students/` folder. Use the `student_name.html` for reference. In fact, feel free to copy as much of the HTML from `student_name.html` into the new file you've created (just don't rename / override that file, as that will cause you some git headaches).

**For Path B (linking to a deployed portfolio):**

- Add only one picture to `img/students/` for the index tile.
- No file in `students/` — the tile's `<a href>` points directly at the deployed `html-student-portfolio` URL.

## Getting Started

### Group Logistics

- Figure out who is going to write whose profile.

- **One person at your table** [forks](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo (top-right "Fork" button on GitHub). They send the URL of their new fork to the rest of the table — it'll look like `https://github.com/<their-username>/deploy-on-day-1-ttpr`.

- **Everyone else at the table** then [clones](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#_git_cloning) **that fork** (not the original repo) to their laptop:

  ```sh
  git clone https://github.com/<table-member's-username>/deploy-on-day-1-ttpr.git
  cd deploy-on-day-1-ttpr
  ```

  > **Heads up:** the *fork's* URL has your tablemate's username in it, not `ttpr-lgcc` or whatever the original repo lives under. If you clone the original by mistake, you won't be able to push your branch.

### Individual Instructions

Now that you have the repo, you'll want to get into it. `cd` into the cloned folder (e.g. `cd deploy-on-day-1-ttpr`). When you type `pwd` into your terminal and the last part of the text that gets returned is `deploy-on-day-1...` you're in the right place. **NOTE: In all the hypothetical examples below, we're writing a profile for Zoe Perez.**

Take a look at `index.html` and `students/student_name.html` in the browser. You can do this many ways but one is by opening finder and right clicking on index.html. Then click on "Open with" then the name of your favorite browser.

#### Make a New Branch

- From the root directory, [checkout a new branch](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Branching). This new branch's name should be the name of the student whose profile you're going to create.

  - For instance, the branch would be titled `zoe-perez`.
  - Note: The `master` branch of a project is NEVER a place to do any work. `master` is considered the build and you never break the build. So make sure you are not working or committing to the `master` branch.

- If you haven't already, switch to the branch you created. To make sure you're where you need to be, type `git branch` in your terminal. It should return the name of your assigned student emphazised with an asterisk and master.
  - For instance, typing `pwd` in the terminal would return:

```text
  master
* zoe-perez
```

#### Add Profile

The next steps depend on which path you picked above.

##### Path A — In-repo profile

- In this new branch, make a new HTML file in the `students/` folder. The file name should be the name of the student you're creating the profile for. **Copy** the contents of `student_name.html` into your new file as a starting template.

  - For instance, we would create a file `zoe_perez.html` in the main `students` folder.

- Still in this branch you created, add the three photos detailed above to the `img/students` folder. The student you're writing the profile for may have to email you their desired pictures or send you links to them, etc.

  - For instance, we would add the pictures titled `zoe_perez_background.jpg`, `zoe_perez_index.jpg`, and `zoe_perez_profile.jpg` to the `students` folder that is inside the `img` folder.

- Once you've completed the profile, open up `index.html`. Use the preexisting template as a model and add a section for your fellow student. Both `<a href>` attributes in the tile should point at `students/<their_name>.html`.

> **⚠️ File-naming rules — read these, they're the #1 source of broken pages:**
>
> 1. **Filenames are case-sensitive on GitHub Pages.** `Zoe_Perez.jpg` and `zoe_perez.jpg` are different files. Pick one convention (lowercase + underscores is easiest) and match the `<img src>` to it *exactly*, including the extension. Locally on macOS this often "works" because the local filesystem is case-insensitive — but it'll 404 once deployed.
> 2. **Do not rename or overwrite `student_name.html`.** It's the template everyone copies from. If you save your work over it, you'll trigger merge conflicts for every other person at your table. *Copy* it to a new file, *edit the copy*.
> 3. **Don't put your files in the wrong folder.** The HTML profile goes in `students/`. The pictures go in `img/students/`. The `<img src>` paths in your profile should be relative — e.g. `../img/students/zoe_perez_profile.jpg`.

##### Path B — Linked deployed portfolio

- Confirm your student's [`html-student-portfolio`](https://github.com/ttpr-lgcc/html-student-portfolio) fork is deployed and reachable at `https://<their-github-username>.github.io/html-student-portfolio/`. If it isn't, walk them through enabling GitHub Pages in **Settings → Pages**.
- Add a single index picture for them to `img/students/` (e.g. `zoe_perez.jpg`).
- Open `index.html`. Duplicate the existing student tile and replace both `<a href>` values with the deployed portfolio URL, the `<img src>` with your new picture path, and the name/tagline text with theirs.

#### Stage and Commit Changes

- Once you're happy with the profile you've created and the changes you've made to the index page, type [git status](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Checking-the-Status-of-Your-Files). The the file you've altered, index.html, should appear in the "Tracked Files" section and the files you've created should appear in the "Untracked Files" section.

- You'll want to [add](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files) then [commit](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes) these changes with a message.

- If you type `git status`, you should see "nothing to commit, working directory clean". If you type `git remote -v`, it should display something like:

| remote | url                                                                 |         |
| ------ | ------------------------------------------------------------------- | ------- |
| origin | https://github.com/table-member's-github-name/deploy-on-day-1...git | (fetch) |
| origin | https://github.com/table-member's-github-name/deploy-on-day-1...git | (push)  |

#### Push Up Your Branch

- Now it's time to [push](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes) to a remote branch. This remote branch doesn't exist yet, you're going to create it by pushing.

  - **NOTE: Do not push to master. Do not type anything that contains the word master!**
  - You're going to push to a branch that is the same name as your local branch.
    - For instance, if we're on the branch zoe-perez, we're going to push to zoe-perez.

- To confirm this push worked you can do two things:
  - Type `git branch -a` — your new branch should appear with a `remotes/origin/` prefix (e.g. `remotes/origin/zoe-perez`).
  - Or go to the URL of the forked repo on github.com and click the **branch dropdown** (the button near the top-left of the file list, usually labeled `main`). Your branch name should be in the list — select it to view your work on the web.

## Next Steps

### Group Logistics

Since your table is going to submit a pull request with all of your tables profiles, you'll need to merge every branch that your table created into a single branch. This branch will contain every profile from your table. The process of merging these branches will probably result in merge conflicts in `index.html` and possibly elsewhere. That's totally okay and expected!

Think about the best way to merge all the branches together. Should one person do it? Should everyone do it in order? Should you merge into a prexisting branch, like `master`, or create a totally new branch? You might be wondering what the best answer is but there isn't a "best answer", just decide on a strategy and go for it!

### Merge Conflicts

When [merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) two branches that both touched `index.html`, git will spit out something like:

```text
$ git merge zoe-perez
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

**Don't panic.** This is the expected outcome — every branch added a tile to the same file in roughly the same place, so git can't tell which to keep. **It wants both.** Your job is to tell it that.

Open `index.html` in your editor. Search for `<<<<<<<`. You'll find a region that looks like this (the names will differ):

```html
<ul>

<<<<<<< HEAD
  <!-- Begin Student -->
  <li class="home-blog-post">
    ... Hessvacio's tile ...
  </li>
  <!-- End Student -->
=======
  <!-- Begin Student -->
  <li class="home-blog-post">
    ... Zoe's tile ...
  </li>
  <!-- End Student -->
>>>>>>> zoe-perez

</ul>
```

For *this lab specifically*, you almost always want to **keep both tiles** — that's the whole point. So delete the three conflict markers (`<<<<<<< HEAD`, `=======`, `>>>>>>> zoe-perez`) and leave both `<li>` blocks in place:

```html
<ul>

  <!-- Begin Student -->
  <li class="home-blog-post">
    ... Hessvacio's tile ...
  </li>
  <!-- End Student -->

  <!-- Begin Student -->
  <li class="home-blog-post">
    ... Zoe's tile ...
  </li>
  <!-- End Student -->

</ul>
```

Save the file. Then:

```sh
git add index.html
git commit            # leave the auto-generated merge message, just save and quit
```

Repeat for every branch your table merges in. If `git status` no longer says "You have unmerged paths.", you're done.

> **Easier alternative if you're stuck:** GitHub's web UI can resolve simple conflicts directly in the browser. After pushing your branch, open the Pull Request page and look for a **"Resolve conflicts"** button. You'll get a side-by-side editor with the conflict markers visible — same idea, no terminal.

## Final Steps

Once every profile is on a single branch that is hosted remotely, it's time to submit a pull request on the original repo. Note: This pull request will be on behalf of your entire table.

- Go to the forked repo on github.com.
- Click the **branch dropdown** (the button labeled `main` near the top-left of the file list) and select the branch that has all your table's profiles merged into it.
- Click the **"Contribute"** button (just above the file list, near the right) → **"Open pull request"**. GitHub will also often show a yellow banner like *"This branch is X commits ahead of `<original-repo>:main`"* with a **"Compare & pull request"** button — that works too.
- On the **Open a pull request** page, double-check the base repo (left dropdown) is the *original* `ttpr-lgcc` repo and the head is *your fork's* combined branch. Write a short description of who's on the branch, then click **"Create pull request"**.

Congratulations, you've completed your first assignment!

Note: From now on, most assignments will be completed in a group but submitted individually. This means that instead of having a **table** fork an assignment, **each student** will fork the assignment, minimizing the merge conflicts you'll encounter in the future.

## Resources

- Companion lab
  - [`ttpr-lgcc/html-student-portfolio`](https://github.com/ttpr-lgcc/html-student-portfolio) — the portfolio repo referenced by Path B
  - [Configuring GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) — how to deploy a static site from a repo
- Git Step Resources
  - [Forking a Repo](https://help.github.com/articles/fork-a-repo)
  - [Cloning a Repo](http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository)
  - [Branching](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Branching)
  - [Adding](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files)
  - [Committing Changes](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes)
  - [Pushing to Remote Branches](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes)
  - [Merging Branches](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merging)
  - [Submitting a Pull Request](https://help.github.com/articles/using-pull-requests#sending-the-pull-request)
- Git Workflow Resources
  - [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
  - [Git Workflow](https://github.com/diaspora/diaspora/wiki/Git-Workflow)
  - [Git Rebase Workflow Explained](http://mettadore.com/analysis/a-simple-git-rebase-workflow-explained/)
  - [How GitHub uses GitHub to Build GitHub](http://zachholman.com/talk/how-github-uses-github-to-build-github)
  - [GitHub Workflow for Submitting Pull Requests](https://openshift.redhat.com/community/wiki/github-workflow-for-submitting-pull-requests)

## Issues

### Common Pitfalls

If you're stuck, scan this list before flagging an instructor — odds are good your symptom is here.

- **"My image isn't showing up."** Check the case of the filename. `Zoe.JPG` ≠ `zoe.jpg`. Also check the path: pictures live in `img/students/`, and from `students/your_page.html` the relative path is `../img/students/<filename>`.
- **"I edited `student_name.html` directly."** That's the template — *copy* it to `students/<your_student>.html` first, then edit the copy. If you've already saved over it, run `git checkout student_name.html` to restore it before committing.
- **"`git push` says `permission denied` or asks for a password that doesn't work."** You almost certainly cloned the *original* repo instead of *your tablemate's fork*. Run `git remote -v`. The URL should contain your tablemate's GitHub username, not `ttpr-lgcc`. If it doesn't, fix it with `git remote set-url origin https://github.com/<tablemate>/deploy-on-day-1-ttpr.git`.
- **"I can't push to `main`/`master`."** Good — you're not supposed to. Branches: `git checkout -b zoe-perez`, then `git push -u origin zoe-perez`.
- **"My branch isn't showing up on github.com."** You probably committed but didn't push. Run `git push -u origin <branch-name>`.
- **"There are merge conflicts in `index.html` and I want to give up."** Read the [Merge Conflicts](#merge-conflicts) section above — for this lab, you almost always want to keep both `<li>` tiles. The `Resolve conflicts` button on GitHub's PR page is often the fastest way out.
- **"My tile shows up but the link goes 404."** Check the `<a href>` in `index.html`. For Path A it's `students/<name>.html` (no leading slash). For Path B it's the full deployed URL ending in `/`.

### Authentication

A common issue is not being able to authenticate with GitHub. You need to use HTTPS/SSH correctly when cloning the repository in order to be authenticated with GitHub. Check out and follow:

- [Setting Up Git](https://docs.github.com/en/get-started/quickstart/set-up-git)
- [HTTPS Cloning Errors](https://docs.github.com/en/get-started/git-basics/troubleshooting-cloning-errors)
- [Setting Up SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
