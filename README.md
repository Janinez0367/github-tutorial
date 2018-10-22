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



---
## Rolling Back Changes