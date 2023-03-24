# Learn-to-git
## brief git commands overview
"git clone" clones the repo from cloud to your local machine__
"git status" will show you changed files and files that are staged for commit__
"git commit" will commit changes in your local git repo. First -m is for the commit name (it is advised to write names as clear as possible). Second -m is for description of that commit.__
"git add" will make file to be staged for commit__
"git restore --staged *file_name*" will make file not to be staged for commit__
you can also write '.' instead of *file_name*. It will stage all changed and added files to commit__
"git restore *file_name*" will restore the unchanged version of the file__
"git push *repo*" will push your local git into cloud__
before you can commit any changes, you have to identify yourself__
"git config --global user.email *email*"__
"git config --global user.name *name*"__
before you can push changes into github you have to generate an ssh key, load public version on github__
and add this ssh key to your ssh-agent__
now I will use git push *repo* with the branch to commit to and keyword 'origin'__
## Setting up a local git repo and pushing it to Github
To create a local git repo you cd into folder and write there git init.__
As usual, you go through process of adding new files and commiting them.__
Then you'll need to push it to github somehow.__
You can do that either by creating a new repo on the site itself or by using a 'gh'.__
'gh' is a Github CLI application for managing github repositories.__
After you've created a repo, you need to connect to that repo.__
'git remote add *name* *link_to_repo*' will connect you to that repo.__
Usually you will give origin to the name if it's the first link.__
To remove the connection, you need to write 'git remote remove *name*'__
You've added the remote connection.__
To push to the github repo, you'd write 'git push -u origin *branch_name*'__
'-u' specifies that we'll upload to origin by default.__
You've pushed your commit to github! Congrats! (my example is Learn-how-to-git-partII)__
## Branching. Merging. Conflicts.
So, you'd also want to create branches. They provide a good version control.__
For example, you may want to write code implementing a new feature in your program.__
We all know that it takes time to wrtie a good clean and safe code. Of course, you wouldn't want to mess up your main branch. So you need a different space to write that code in.__
That's why you'd create "feature" branch where you do all this work on your new feature.__
All commits to the branch are local.__
To create a new branch, you write 'git checkout -b *branch_name*' (it will also move you to that branch).__
All files from the branch you're creating from will be also in the new branch.__
To move between branches you write 'git checkout *branch_name*'.__
To see all branches you have you write 'git branch'__
So, imagine you've done all the work and now you want to merge, let's say, 'feature' to 'main'.__
'git merge *branch_name*' will merge *branch_name* into the branch you're currently in.__
If you want to merge it in github, you will need to pull a request (PR for short). The team of devs will review your code, comment some lines and the code will just go through a check.__
If everything is fine, the PR will be merged.__
When branching, there may be a conflict. It happens when the same parts of files are changed.__
In this case, you will see something like 'merge conflict'.__
In the file, where there is conflict, you will see '<<<<<<<<<<<<', '>>>>>>>>>>' and '========='.__
The '=======' will separate the change from the current branch and incoming branch.__
The '<<<<<<<' is the current branch change.__
The '>>>>>>>>>>' is the incoming change.__
You or the team will just need to change the code so that it satisfies you or a team of devs.__
When you've done the change, you do a commit: 'git commit -am...__