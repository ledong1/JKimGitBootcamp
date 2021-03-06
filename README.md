# JKimGitBootcamp
Git and Github exercises compiled and presented by Je Hyun Kim for CUS1151.

## Setting up
### Downloading
* Mac - http://git-scm.com/download/mac
* Windows - http://msysgit.github.io/
* Linux - http://git-scm.com/book/en/Getting-Started-Installing-Git

Check if git is installed correctly. Open your terminal and type the following command
```
$ git --version
```

### Setting up for github
First, create a github account at https://github.com if you don't have an account already.

In your terminal, copy and paste each of these commands and replace the information inside quotes. 
```
$ git config --global user.name "Your name here"
$ git config --global user.email "your_email@example.com"
```
* (Optional more info https://kbroman.org/github_tutorial/pages/first_time.html)

## Main presentation
https://rogerdudler.github.io/git-guide/

## Exercise
### Exercise 1 (Basics).
1. Create a github repository called hello-world on http://github.com <br />
![step1](https://help.github.com/assets/images/help/repository/repo-create.png) <br />
![step2](https://help.github.com/assets/images/help/repository/create-repository-name.png) <br />
![step3](https://help.github.com/assets/images/help/repository/create-repository-init-readme.png) <br />
2. Clone the github repository to your computer.
Find the link to your repository by clicking the following button: <br />
![clone_button](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png) <br />
![clone_url](https://help.github.com/assets/images/help/repository/https-url-clone.png) <br />
Copy the url to the github repository and use it in the following command:
```
$ git clone "URL_TO_THE_REPOSITORY" #Copy the repository locally
$ cd hello-world #Move directories to hello world
```
Then, create a text file called "myFile.txt" in that location (using any text or code editor) with some text in it (for example, Hello World!).
```
$ git status #View the state of the repo
$ git add myFile.txt #Stage a file (ready to add to the repository)
$ git commit -m "Commenting my first commit!" #Commit into the head of your local repository
$ git push origin master #Push your changes onto the remote repository (on github.com)
```

### Exercise 2 (Branching).
```
$ git branch #View all branches in repository
$ git branch feature1 #Create a new branch
$ git checkout feature1 #Switch branches
```
You've now created a branch called feature1. Make a new text file (name it something.txt) in the repository and save it.
Now do this process to add and commit the changes:
```
$ git add something.txt
$ git commit -m "Added something"
```
Now, swap back to the master branch and merge your feature1 to it.
```
$ git checkout master
$ git pull
$ git checkout feature1
$ git merge master
$ git add -A
$ git commit -m "Created feature1 branch"
$ git push --set-upstream origin feature1
```
Now go to your github repository, navigate to your branch and pull. <br />
![pull1](https://help.github.com/assets/images/help/pull_requests/branch-dropdown.png)
![pull2](https://help.github.com/assets/images/help/pull_requests/pull-request-start-review-button.png)
<br/>
On github now, you will be able to merge the pull request. <br/>
![pull3](https://f.cloud.github.com/assets/676185/316946/e8c42c4c-984e-11e2-8a09-5a977652028a.png)

### Exercise 3 (Contribute to this repo)
Fork this repo on top of this page by pressing this button:<br/>
![fork1](https://help.github.com/assets/images/help/repository/fork_button.jpg)<br/>
Now, this repository is copied onto your own github account. Clone the forked version onto your computer
```
$ git clone "URL_TO_FORKED_VERSION"
$ cd JKimGitBootcamp
$ git remote add upstream https://github.com/je-hyun/JKimGitBootcamp.git #This line adds a link to the original version
$ git branch addMyName
$ git checkout addMyName
```
Create a file named after your own name (e.g. Your_Full_Name.txt) to that local git repository. Put the name of your favorite song or book in it.
```
$ git add "Your_Full_Name.txt"
$ git commit -m "Add my favorite song."
$ git pull upstream master
$ git push origin master
```
Now, from github, you can make a pull request to the original repository.

## Summary
### Basic commands
* git clone URL # Clones a remote repository
* git status # Views which files were staged for changing
* git add FILE # Adds a file to the repository
* git commit -m "Comment" # Commits to local repository with comment
* git pull origin master # Pulls changes from the remote
* git push origin master # Pushes changes to the remote
### Branching
* git branch # View all branches
* git branch BRANCHNAME # Create a new branch
* git checkout BRANCHNAME # Swaps branches
* git merge BRANCHNAME # merges another branch into the current one

### Other resources
* Git cheat sheet reference https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf
* Adding collaborators on github- https://stackoverflow.com/questions/7920320/adding-a-collaborator-to-my-free-github-account
* Full collaborative workflow- http://www.eqqon.com/index.php/Collaborative_Github_Workflow
