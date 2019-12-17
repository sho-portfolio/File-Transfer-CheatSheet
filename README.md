# File-Transfer-CheatSheet
How to transfer files between Google-Storage-Buckets, Local-Machine, Google-VM/Google-Compute-Engine and GitHub

| From                   | To                     | Command
| ---------------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------- 
| Internet               | Local Machine          | ```wget https://raw.githubusercontent.com/sho-portfolio/sample-repo/master/fileA.txt```    
| Github                 | Local Machine          | ```wget https://raw.githubusercontent.com/sho-portfolio/sample-repo/master/fileA.txt``` <br/> [or] ```git clone https://github.com/sho-portfolio/sample-repo.git```                                                                                                              
| Github                 | Google Storage Bucket  | ```wget https://raw.githubusercontent.com/sho-portfolio/sample-repo/master/fileA.txt``` <br/>[then] ```gsutil cp downloads/dataTest.txt gs://bucket-sho```                                            
| Github                 | Google Virtual Machine | ```wget https://raw.githubusercontent.com/sho-portfolio/sample-repo/master/fileA.txt``` <br/>[or] ```git clone https://github.com/sho-portfolio/sample-repo.git```                    
| Local Machine          | Githib                 | See #0 below <br/> 1) ```cd your-project-directory``` <br/>2) ```git init``` <br/>3) ```git add . or git add ['filename']``` <br/>4) ```git commit -m "your comment"``` <br/> 5) ```git remote add origin https://github.com/yourusername/your-repo-name.git```<br/>6) ```git push origin master```<br/> see #1 below
| Local Machine          | Google Storage Bucket  | ```gsutil cp downloads/dataTest.txt gs://bucket-sho```
| Local Machine          | Google Virtual Machine | ```gcloud compute scp dataTest.txt instance-sho:~```
| Google Storage Bucket  | Local Machine          | ```gsutil cp gs://bucket-sho/myfile.txt foldername/fileA.txt``` 
| Google Storage Bucket  | Google Virtual Machine | ```gsutil cp gs://bucket-sho/myfile.txt foldername/fileA.txt```
| Google Virtual Machine | Github                 | https://www.tutsmake.com/upload-project-files-on-github-using-command-line/
| Google Virtual Machine | Local Machine          | ```gsutil cp downloads/dataTest.txt gs://bucket-sho``` <br/> [then] ```gsutil cp gs://bucket-sho/dataTest.txt foldername/fileA.txt```
| Google Virtual Machine | Google Storage Bucket  | ```gsutil cp downloads/dataTest.txt gs://bucket-sho```


# Notes
* Mac OS does not come with wget installed.  To install wget run the following command in Terminal: ```brew install wget```
* To install git on a machine (local or virtual) run the following commands in Terminal: ```sudo apt update``` then 
```sudo apt install git```
* useful tutorial for copying fr=iles from and to github
* #0 a much easier way to upload files
<br/>[https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/]
<br/> ```cd <folder you want to d/l your repo to>```
<br/> ```git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY```
<br/> ```git clone https://github.com/sho-portfolio/sql-cheatsheet.git```
<br/> make changes to existing files or add new ones
<br/> ```git status``` this will show you any changes made
<br/> ```git add --all``` (or git add <filename>)
<br/> ```git commit -m "commit comment goes here..."```
<br/> ```git commit```
<br/> ```git log``` (shows you the history of your repo)
<br/> ```git push```


* #1 if you are getting errors when trying to ```git push master origin``` try these commands in the terminal
<br/>[https://stackoverflow.com/questions/28429819/rejected-master-master-fetch-first]
<br/>```git fetch origin master```
<br/>```git merge origin master```
<br/>```git fetch origin master:tmp```
<br/>```git rebase tmp```
<br/>```git push origin HEAD:master```
<br/>```git branch -D tmp```
<br/>```git push origin master```
