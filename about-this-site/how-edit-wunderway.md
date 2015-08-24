---
layout: page
section: how
categories:
tags:
title: How To Edit The WunderWay
---

The WunderWay is intended to be collaborative and continuously improved. Any change or addition can be suggested by anyone, and requires peer review before being merged into the official WunderWay.

To help with this, we use Github's [pull request workflow.](https://help.github.com/articles/using-pull-requests/) This allows us to keep all the different versions of the content that have ever existed, track changes, and discuss them. It also allows us easily catch and fix any mistakes - so don't worry about breaking it.

## The Update Process

All updates, whether editing existing content or adding new content, is done using issues and pull requests in GitHub.

If you have an idea for new content, a new process or a new tool then raise an issue and include a clear description of your request and the reasons behind it.

If you are creating new content or editing existing content then this can be raised as a pull request.

The process is simple:

 - Raise a pull request (PR) or issue in GitHub
 - The PR or issue is reviewed
 - Comments, questions, queries and discussions are recorded in GitHub
 - If the change is accepted:
	 - An issue will require a pull request to be created to add or edit the content
	 - A pull request will be reviewed by those with responsibilities for that area of the WunderWay
	 - When the pull request is merged then any relevant issue will be closed
	 - Updates will be automatically posted in the WunderCafe room in HipChat

It's important that we have a review process for all new content. The WunderWay is audited annually and we need to log:

 - The reasons and discussions behind the edit or new content
 - The value is brings
 - The impact. Does this need to be communicated?
 - The impact on our [objectives](/about-this-site/quality-management-system/quality-objectives/). Does this change need to be measured and is there a process in place for that?

## Preparing To Work On The WunderWay

### Editing The WunderWay On Github
You can simply work on the Github website, without needing to set up anything on your own computer:

Either:

1. Navigate on the [WunderWay](http://way.wunder.io) to the page you want to edit
2. Click the link at the top of the page, in light grey, that says 'Edit This Page'

Or:

1. Go to the [WunderWay repository](https://github.com/Wunderkraut/WunderWay) on Github
2. Navigate to the page you want to edit, clicking on the folders until you find the filename you want. Click on that. For example, this page can be edited at https://github.com/Wunderkraut/WunderWay/blob/gh-pages/how/how-edit-wunderway.md

You will then be viewing the source of the page on Github. To edit this:

1. Click the Pencil icon to 'Edit this file'. Make the changes you want.
2. At the bottom of the screen, in the 'Propose Changes' section, add a description of the changes you've made.
3. Click the 'Propose Changes' button.
4. Your pull request will appear on the WunderWay [pull requests page.](https://github.com/wunderkraut/WunderWay/pulls)
5. A notification of this pull request will appear in the WunderCafe Hipchat room. Reach out to specific people to ensure they see your pull request.

### Editing The WunderWay On Your Local Computer using the Github app
1. Download and install the [Github for Mac](https://mac.github.com/) software.
2. Download and install a text editor of your choice. eg. [Sublime Text](http://www.sublimetext.com/)
3. Open the Github app and, on the repositories screen, select 'Wunderkraut' repositories.
4. On the 'Wunderkraut/WunderWay' repository select 'Clone to Computer'
5. Select a suitable folder to save the files in.
6. Open your text editor. From the File menu choose 'Open...'. Select the folder where you cloned the WunderWay repository.
7. In Sublime and similar text editors, you'll see the folder structure of the WunderWay on the left hand side. Find the file you want to edit, and make the changes. Select File>Save when you are done.
8. In the Github for Mac application, under 'changes' it will show that you have 'uncommitted changes'. Type a heading and description about the changes you made. Click Commit.
9. You can make many edits like this offline. When you are back online and want to open a pull request for your changes you follow the instructions on [Create Pull Requests with GitHub for Mac](https://github.com/blog/1946-create-pull-requests-with-github-for-mac) ![Demonstration of a pull request](https://cloud.githubusercontent.com/assets/13760/5697198/35b8c866-999f-11e4-91c1-7af538f2ced5.gif)
10. Your pull request will appear on the WunderWay [pull requests page.](https://github.com/wunderkraut/WunderWay/pulls)
11. A notification of this pull request will appear in the WunderCafe Hipchat room. Reach out to specific people to ensure they see your pull request.


#### Previewing your WunderWay changes on your local computer
1. Navigate to the top WunderWay folder in your terminal
2. Install Jekyll by running ``` $ gem install jekyll ```
3. You you encounter an error, you may need to run ``` $ sudo gem install jekyll ```
4. In the same directory, run ``` jekyll serve ```. This compiles the jekyll site and makes it availiable on http://localhost:4000
5. If you want Jekyll to recompile the site every time you save a file, run ``` jekyll serve --watch ``` instead


## Reviewing and merging pull requests
For instructions on how to review and discuss the proposed changes see [Using pull requests.](https://help.github.com/articles/using-pull-requests/#reviewing-proposed-changes)

After a consensus has been agreed, and you have the permissions, you'll want to merge the pull request into the official WunderWay. For instructions on how to merge and close a pull request see [Merging a pull request.](https://help.github.com/articles/merging-a-pull-request/)


## Formatting
The WunderWay uses a formatting syntax called 'Markdown' to generate the content. It's simple to use once the basic syntax is learned. You can read Github's [Introduction to Markdown](https://guides.github.com/features/mastering-markdown/) and you can find a full description on the syntax at http://daringfireball.net/projects/markdown/syntax

## Creating New Pages
If you need to create a completely new page, you can create a new file in the right section folder in WunderWay. Call the file 'your-file-name.md' where your-file-name can be anything you like. The '.md' file extension is important.

At the very beginning of your file you need a few lines of text called 'front-matter'. These look like this, and you can copy and paste this as a template to start with and edit as you need...

    ---
    layout: page
    section: how
    exclude_from_search: false
    title: How To Claim Expenses
    ---

This tells the system that builds the site what type of file it is, what section it's in, the categories it's in, and the title. The Tags will help with navigation.

### Front-matter options

When writing a front-matter section for a new page, here's some options and suggestions for you.

- **layout**
  - ***page*** - A regular page
    - You will want to use this mostly.
  - ***section*** - An index page to a (sub-)section of the site.
    - Section pages have a bullet-point list (organised alphabetically, ascending) of sub-pages automatically added at the bottom.
    - It's probably a good idea (though not required) to name these files index.md and put them inside a (sub-)directory named for the section
- **section**
  - The named section of the site
    - For naming convention, use machine-friendly style i.e. lowercase a-z, 0-9 and - characters only
    - It may be a good idea (though not required) to use the name of the directory of the section as the section name
  - both *section* and *page* layout pages should use the section designation
- **title**
  - the page title displayed on the page and when the page is included in any lists
- **exclude_from_search**
  - include and set to 'true' to exclude page from search

Some [other front-matter options](http://jekyllrb.com/docs/frontmatter/) are available, but we don't really need to use them in WunderWay.
