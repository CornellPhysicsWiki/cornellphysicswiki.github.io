---
title: Contributing Guide
layout: post
---
<link rel="stylesheet" href="main.css">

* TOC
{:toc}

## How to Contribute

This site was started by students just like you, and we need your help in keeping it up-to-date and adding new content. If you want to update 
this website, you can either: 
- Edit the code directly
- Submit an issue ticket
- Fill out this [information form]() and a website admin will update the website content.

## Create an Issue Ticket

We always welcome new ideas, suggestions, and comments. You can add an issue ticket [here](https://github.com/CornellPhysicsWiki/cornellphysicswiki.github.io/issues). You will need to create a GitHub account to make an issue ticket.

## Edit the Website Code

You can edit the website directly following these steps:

- Create a GitHub account
- Clone the repository on your local computer
- Create a new branch off of master
- Make your changes
- Submit a pull request

### 1. Create a GitHub account

Go to [GitHub](https://github.com) and sign up. You’ll need to confirm your email address before you can do anything else.

### 2. Clone the repository on your local computer

There are two ways to make changes: you can either make a local copy of the codebase on your computer and edit it, or you can edit the code on the Desktop
version of GitHub. Here, we will discuss the first method. This method especially useful since it allows you to run your changes locally and test that everything
works before attempting to push your changes to the public website.

On your computer, open a terminal and go to the folder where you want to store the website files using `cd` commands.

Go the website [Github repository](https://github.com/CornellPhysicsWiki/cornellphysicswiki.github.io). Click the "Code" button at the top right. There 
should be a small pop-up window that says "Clone" and a URL, as shown below. Copy this URL and go back to your terminal. Enter `git clone [URL]`.

<img src="/imgs/clone_repo.png">

Now a copy of all the website files should be downloaded onto your computer!

### 3. Create a new branch off of master

The files for the public-facing website are all on a branch called `master`. Only the website administrators can directly edit the website on the master branch.
If you are not an administrator, then you will have to make your changes on a separate branch and request to merge your changes into `master`.

Making a new branch is especially easy on the Desktop version of GitHub. Go back to the website [Github repository](https://github.com/CornellPhysicsWiki/cornellphysicswiki.github.io). On the top left, there should be a gray box that says `master`. Click on this, and in the text box below, type what you want
to name your new branch. Make sure that no other existing branch has this name. After that, an option should show up saying `Create branch: [your branch] from master`. Click on this, and you will have created a branch where you can make all your changes!

<img src="/imgs/make_branch.png">

Now you will need to switch to your new branch on your local computer, so that all your changes will be stored there instead of `master`. In your terminal, enter:<br/>
`git pull`<br/>
`git checkout [your branch]`

### Make your changes

Now that you are pretty much all set up, you can start making your changes! The website pages are written using Markdown. Markdown is a simple tool for adding formatting to plain text documents. A quick guide to the syntax can be found [here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax). It is intended to be simple to use and easy to read.

There’s also some Markdown formatting specific to the software we’re using for this wiki, [Jekyll](https://jekyllrb.com). In particular, you might notice a section like this at the top of every page:

```
---
title: PHYS 1116 - Mechanics and Special Relativity
layout: post
---
```

This is just metadata that tells Jekyll what page template to use and what the page title is.

After you make your changes, you may want to run the website locally to see if everything works. The website is built with a software called Jekyll, so if you clone the repository and try to preview, you’ll just get an preview of the markdown. Here’s how to fix this.

- [Install Jekyll](https://jekyllrb.com/docs/installation/#guides) on your computer.
- `cd` (the command) into the directory where you cloned the github repo.
- If jekyll is installed correctly, when you run `jekyll serve` or `bundle exec jekyll serve`, you should see a serving running message. 
- Navigate to the server address in your browser (normally “127.0.0.1:4000”). You should see the page rendered.

### Submit a pull request

You've created some amazing new pages and changes, and now you want to add them to the public wiki website! First, you will need to commit/save your changes to your branch. In your terminal:

- Go to the folder where all the website files are store using `cd` commands
- Enter `git add -A`
- Enter `git commit -m [summary of your changes in a few words]`
- Enter `git push`

