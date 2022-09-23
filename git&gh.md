# git

1. `touch .gitignore` create git ignore file
2. `git init` intialize directory with git
3. `git add [file]` add files to git(. means all)
4. `git commit -m [message]` commit the files
5. `git tag [tag]` tag version of this files
   `-d` delete tag
   `-v` view tag
6. `git push [repo_name] [branch]` push the files to github
   `git push origin master` master branch
   `git push --set-upstream [repo_name] [branch]` renew the remote branch name
7. `git push [repo_name] --tags` push the tags to the github
8. `git clone [url]` clone repo from github
9. `git status` check status
10. `git log [branch]` check log
11. `git rm --cached` remove files from git
12. `git checkout [tag]` to specific version
13. `git restore [file]` restore files
14. `git remote add [repo_name] [url]` add repo url into local git
15. `git remote -v` show that match between repo and url
16. `git remote rename [repo_name1] [repo_name2]` change remote repo name
17. `git remote remove [repo_name]` delete remote repo
18. `git fetch [repo_name]` synchronize the remote repo and local repo
19. `git pull [repo]` pull the remote repo down to the local
20. `git branch [branch]` create new branch
    `-d` delete branch
    `--no-merged` no merged branch
    `--move [branch1] [branch2]` change branch name
21. `git checkout [branch]` switch to existing branch
22. `git switch [branch]` switch to existing branch
23. `git merge [branch]` merge branches
24. `git rebase [branch]` merge branches and keep now branch is the head
