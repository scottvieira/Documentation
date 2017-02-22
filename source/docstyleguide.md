CORAL Documentation Style Guide
-------------------------------

### About the Style Guide ###

The purpose of the style guide is to help keep the documentation consistent in style while at the same time providing tips for contributing to the CORAL Documentation Project (CDP) and other relevant information.

### Helping Out

The CDP is a great way to participate in a small or big way as time allows.  Take something in the documentation that you would like to improve and help out, whether it is editing, adding new content, or just sharing a tip.  All the information needed to get started is found below.  When finished you will need to submit a pull request in GitHub for any changes.  The Web Committee will review these pull requests and merge them into the documentation as they are approved.  For any suggestions or questions about helping out, please email us at [help@coral-erm.org](mailto:help@coral-erm.org).  

### Setting Up ###

The CDP is managed in a repo on GitHub found at [https://github.com/Coral-erm 
](https://github.com/Coral-erm  "https://github.com/Coral-erm ").  The project uses the [Sphinx Python Documentation Generator](http://www.sphinx-doc.org/en/stable/) and [ReCommonMark](http://recommonmark.readthedocs.io/en/latest/).  The documentation files are edited in a combination of [reStructuredText](https://en.wikipedia.org/wiki/ReStructuredText) and [Markdown](https://en.wikipedia.org/wiki/Markdown), both markup languages supported by GitHub.  In addition, [Read the Docs](https://readthedocs.org/) is used for hosting the documentation and providing additional documentation conversion and indexing tools.  

### Editing Markdown

There are a lot of great resources online about Markdown, but to get started you may want to use a Markdown editor.  There are many available free, but the best one for you will depend on your operating system.  One suggestion for Microsoft Windows would be [MarkdownPad](http://markdownpad.com/).      

### Basic Instructions on Getting Started with GitHub

**Git and Github Documentation Workflow Procedures**

*Note: Except as noted the following instructions are for Microsoft Windows using the command line prompt. *

*These instructions presume you have the correct software installed.*

1. Go to a command line editor in Windows.

2. The following step will not be relevant the first time through this process.  Use **`git fetch`** and then **`git pull`** on your master branch to make sure it is up to date before creating your working branch in step 7 below. 

3. Create a working folder.  In a windows command line editor this would be:  **`md Work`**, where "Work" can be whatever you want to call your folder. (for Mac: `mkdir Work` )

4. Move inside your "`Work`" folder.  Command: **`cd Work`** or whatever your path is **`cd c:\Work`**

5. There are different ways to do this, but probably the easiest to get started would be to run the following command to clone a copy of the master version of the Documentation repo.

Command: **`git clone`**[ https://github.com/coral-erm/Documentation](https://github.com/coral-erm/Documentation)

Running this command will do a few things including identifying what github account and repo you are working with and by cloning a master version of the repo to your folder.  It will also initialize your folder for use with the application Git.  This process creates some hidden files and folders that track changes, active branches, and more.

6. Change your working folder to Documentation.  In our example, **`cd\Work\Documentation`**

7. You should now be in the master branch of the repo.  You can use **`git status`** to see what branch is currently selected.  You could make changes to the master branch, but when you copy these changes back to github you would be directly merging your changes into the master branch of the repo.  Instead what you want to do is create a branch of the master version, so that later on when you copy your changes back to github, you have to go through another step, in github lingo a "push request," to request that your changes be merged into the master branch.  This allows for you to make sure you don’t inadvertently write over another person’s changes in the master branch.  Use the following command to create a new branch from the master.  Command: **`git checkout –b <branchname>`**   (If the branch name already exists use **`git checkout <branchname>`**).  You can now start making changes to your files.  Feel  free to do this by commandline or gui.  For us we are going to use Windows Explorer to navigate to the following folder.  Taking our example earlier.  **`C:\Work\Documentation\Source`**

You will notice that there are two folders under Documentation.  Build and Source.  Most users will be working exclusively with the Source.  This is where the individual files for the documentation are to found.  There are two files types of importance:  .md = Markdown files and .rst = Restructured Files.  Restructured Files are Python files used by the Sphinx Documentation Generator.  We are using only one of these files at this time.  This file is being used primarily to create our Table of Contents structure.  For now, you will be editing primarily the Markdown files.  If using Microsoft Windows, you can use the recommended MarkPad 2 for Windows application to open the files.

8. Make whatever edits you need to the Markdown files and be sure to save your changes.  Be sure to save your changes.  

9. Go back to your command line and change your working directory to the following.  For our example,  **`C:\Work\Documentation`**

10. Now you are ready to copy your changes back to github.  Remember you are working with a different branch to the repo than the master branch.

11. First, use the following command to update the content you are about to commit to github.  Command: **`git add *.*`   **You can use this to just add whatever files you have changed.  I usually use *.* to gather any files changed.  We are using the hidden file `.gitignore` to ignore adding any files from the `/build` subfolder.

12. You are now ready to commit your changes to github.  Type the following command while substituting for "text description" a meaningful description of what changes you made.  Command: **`git commit –m “text description”` **

13. Now you are ready to push your commit to the repo with the following.  Use the following command: **`git push https://github.com/coral-erm/Documentation`**

The command **`git push` **will work alone when you have an established connection.

14. Now go to your github account and navigate to the `https//github.com/coral-erm/Documentation` repo.  You should see your latest commit and branch showing up in the branch dropdown list.  The branch list is on the left side under the code tab.  Since you were using a different branch you are now ready to submit a pull request to merge your latest commit to the master branch.

15. Click on your branch to open it up.  Once open you can use the Compare feature on the right side to review your changes and any possible conflicts.  When ready click on the Pull Request button next to the Compare button. 

16. Write a message related to your pull request.  This can be a request to merge and/or notes about the changes.

17. You should receive the message "This branch has no conflicts with the base branch."  If so, and you have permission to do so, go ahead and select the green “Merge pull request” button to merge your changes into the master.  Other options here include adding a comment or closing the pull request.  

Note:  Admin rights are required to merge the pull request.  Only members on the Web Committee and Steering Committee have these rights, so in this case outside parties submitting a pull request will require someone on our committee to review, approve, and merge the changes.  

18. After clicking on the "Merge pull request" button click the “Confirm merge” button.  You should receive the message “Pull request successfully merged and closed.”  Go ahead and delete your branch by pushing the “Delete branch” button.  Doing this will keep your workflow cleaner.  Likewise, creating a new branch when needed will keep your working files closer to the master branch.   Once you have committed your changes they will be updated in generally less than a minute at [http://docs.coral-erm.org/](http://docs.coral-erm.org/).  If changes don’t appear right away, try refreshing the cache in your browser.

19. You have finished the process of cloning the repo, creating a branch, making updates to the source files, committing the changes in your new branch to the repo, and finally merging those changes into the master branch.  


### File Structure and File Naming Conventions ###

#### Images ####

1) Create a subfolder under /img using the same name as the markdown file in which the images will be used.  

For example, the following folder name for organizations.md

	/img/organizations/


2) Add images to the subfolder created in step 1.  Name the images with a prefix identifying the markdown file they are associated with, separated Uppercase letters with a brief description of the image. Note: The underscore character causes GitHub to incorrectly process the image filenames in Markdown, which leads to problems in building files in the ReadtheDocs.

For example: **organizationsAccountsView.png** for a a screenshot of the Organization's module accounts form.

WARNING! Image file names are case sensitive.  This includes the file extensions.  Be consistent in keeping all file extensions in lowercase.  For example **sampleFile.png**

3) Add reusuable images such as icons to the /img/general folder.


