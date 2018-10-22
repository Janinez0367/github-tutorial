# GitHub Tutorial

_By Janine Zhang_

---
## Git vs. GitHub

**GIT**  

* Version control: keep “ snapshots” of code
* _Does not require github_

**GITHUB**

* Store code in the cloud
* Visually track changes
* Easily collaborate on files
* _Requires git_

---
## Initial Setup

Setting up a _**GitHub**_ account :
1. Go to [github.com](Github.com)
2. On the top right corner click sign in or sign up(insert picture)

Creating a SSH Key: (To connect to your remote)
1. Login into your [Github](github.com) account that you have or just created.
2. Click your profile icon on the top right corner and click setting
3. On the left sidebar click SSH and GPG keys
4. Click New SSH Key
5. Now your can go to [Cloud9](c9.io/login) or your local
6. Go to the top-right and press the (GEAR ICON)
7. Select SSH Keys Tab and copy the _**2nd**_ SSH key and paste it to GitHub --> press add SSH key 
 Go back to cloud9
1. Open your IDE (Workspace)
2. type "ssh -T git@github.com" in your bash  
--> should show up  something like this  
```Hi <your username>! You've successfully authenticated, but GitHub does not provide shell access._```


---
## Repository Setup

Every time your create a new folder you can initialize it (Basically means that you can push things from Cloud9 to Github)

How to initialize your Repo (Folder)  
1. When ever you create a folder you have to go into that folder (In this case on cloud9 your can ```cd <folder name>```)
2. Now your can type ```git init```

How to make your remote repo on Github  
1. Go to [github.com](Github)
2. Top-right click the (PLUS BUTTON)
3. Select New repository 
      * Repository name: ```<Folder Name>```  
      **MUST BE THE SAME NAME AS THE FOLDER FROM CLOUD9**
4. CLick Create repository  

How to add & commit for the first time using the ssh key 
1. Now make a file in your folder (MAKE SURE YOU ARE IN THE CORRECT FOLDER)  type ```touch <file>``` if your using Cloud9
2. Now type ```git init``` WHEN YOUR IN YOUR FOLDER NOT FILE
3. Now type ```git add <FILENAME>```
4. Now type ```git commit -m "< A message of the things you just did in the FILE>"```
5. Now Copy this line ``` git remote add origin git@github.com:<username>/<filname>.git``` from github where you just create your repository and paste it into cloud9
6. Now copy and paste ``` git push -u origin master```  
``` git push -u origin master``` is when you first tell cloud9 that from now on you want to push all your commit to github and the next time you want to push you just type ``` git push ``` instead

---
## Workflow & Commands
Checking the your status on where your at ,add ,commit and push is a way to have a duplicate of your file 

 Checking Status
 * type ```git status```
   * This will tell you if everything has already been move to github or not 
    * It will show you RED if it hasn't been Push to github 
   * It will be Green if you push the file BEFORE but later on made some changes but didn't push again
 
Adding your file 
* type ```git add .```
  * This will add your current/entire directory to the stage
* ```git add <FILENAME>```
  * This will add the file to the stage for it to be commited

Commiting a file
* Type ```git commit -m "message"```
  * This take a 'snapshot' of the files on the stage 
  * The message should be presnt-tense and describe what was modified in the snapshot

Pushing the File
* Type ``` git push```
  * Thsi will push the files to Github 
  * Only if the file was commited

---
## Rolling Back Changes

##### _**Undoing edits/add/commit/push**_

After you push your file to github it is possible to do the opposite and also what you did before you push anything can be changed too.

Undo edits 
* Type ```git checkout --<filename>```
  * This will undo your edits only when you added them to the stage
 
Undo add
* Type ```git reset HEAD <FILENAME>```
  * This will undo what you added to the stage AFTER you commited the file 
  * This will **NOT** undo any edits that were made

Undo commits
* Type ```git reset --soft HEAD~1```
    * This will undo your commit when you have already pushed it to github

Undoing add from push 
* Type ```git reset HEAD~1```
  * This will undo commit and add all at once 

Undoing edits from push 
* Type ```git reset --hard HEAD~1```
  * This will UNDO commit ,add , and edit all at once