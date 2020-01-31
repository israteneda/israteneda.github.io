# Config development enviroment

1. clone repository
2. change to `source` branch with `git branch source oirgin/source`
3. change directory to clone repository folder
3. install hugo framework
4. run with `hugo serve`
5. create a empty `public` folder
6. inside of `public` run `git init` to create a new repository inside a repository
7. link the `public` local repository with the remote repository with `git remote add origin <url>`
8. run `git pull origin master`
9. change to parent directory and edit what do you want.
10. run `hugo` to compile the changes.
11. run `deploy.sh`script to deploy the changes.