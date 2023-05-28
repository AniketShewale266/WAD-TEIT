open github and create a repository

//When you set your user.email and user.name in GitHub, you are identifying yourself as the author of the code in your repository. 
This information is used to track who made changes to the code, and it can also be used to notify you of changes to the code.
1. ```git config --global user.email "your_email@example.com"```

2. ```git config --global user.name "Your Name"```

open github and click on settings-> ssh and GPG keys-> generate ssh keys
  ```ssh-keygen -t rsa -b 4096 -C "abhisheksinha12377@gmail.com"```
  press enter
  press enter
  
  ```eval "$(ssh-agent -s)"```
  
  ```ssh-add ~/.ssh/id_rsa```
  
  ```clip < ~/.ssh/id_rsa.pub```
  
 
//This command will create a hidden directory called .git in the current directory. This directory will contain all of the data and metadata that Git needs to track your project's history.

3. ```git init```

//The git add command is used to add changes to the staging area. The staging area is a temporary area where you can collect changes before committing them to the repository.

To add all of the files in the current directory to the staging area, you can use the git add . command.

4. ```git add .```

//The git status command is used to show the status of the current working directory and the staging area. 
It will show you which files have been modified, which files have been added, and which files have been deleted. It will also show you which files are not being tracked by Git.

5. ```git status```

//The git commit -m "first" command is used to create a new commit in a Git repository. The -m flag specifies the message for the commit. In this case, the message is "first".

When you create a commit, you are essentially taking a snapshot of your project at a particular point in time. This snapshot includes all of the files in your project, as well as any changes that you have made to those files.

6. ```git commit -m "first"```

//The git remote add origin command is used to add a new remote repository to your local repository. The remote repository is typically a public repository on a service like GitHub or Bitbucket. Once you have added a remote repository, you can use it to fetch and push changes to your local repository.

7. ```git remote add origin https://github.com/AbhishekSinha7/test1.git```

//remove origin if existed 

8. ```git remote rm origin```

//The git push -u origin main command is used to push the current branch of your local repository to the main branch of the remote repository named origin. The -u flag tells Git to set up a tracking relationship between the local and remote branches. This means that any changes you make to the local main branch will automatically be pushed to the remote main branch, and vice versa.

9. ```git push -u origin main/master``` 
