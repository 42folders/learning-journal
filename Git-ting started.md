# Adding a new git repo to GitHub
I've just added a new git repo to my Github with the following code that Github provides as a guide:

To use these lines, open up a Terminal window. At the command line, change directory to the folder which you want to create a local repo:
``` 
> cd <path_to_folder_for_repo>
```

To quickly get the filepath of the folder in which you want to create a git repository, in the Finder, while holding down the 'Option' key, right click on the folder, select the "Copy "xxxx" as Pathname" 

Once you've changed directories, enter each of these commands in sequence: 

```
echo "# news-classifier" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/42folders/news-classifier.git
git push -u origin main
```

These lines will create a README markdown file with the header "# news-classifier". It will also initiate a local git repository with the markdown file, make the first commit, name the branch you're on as "main", add the remote repository with the name "origin", and then push the contents to it. 

# Must-know commands

To check what files are being tracked by git and what aren't:
```
> git status
```

To add a new file to the local repository
```
> git add <new_file_to_be_tracked>
```

To make a commit: 
```
> git commit -m "my commit message"
```

To push commits to the remote repo (to branch called "main"): 
```
> git push origin main
```


##**I have an existing folder that is in the local repository that isn't showing up in remote. How do I add the folder?**

The folder cannot be empty. It needs to have at least 1 file in it. Just do an 'add':
``` 
> git add /data
```
Then commit and push as usual. 


## **How do I know what is my remote origin's name?**
The default name is usually 'origin'

To find out what is the remote origin, enter this at the command line;  adding the -v flag displays its URL:
```
> git remote -v
origin https://github.com/42folders/news-classifier.git (fetch)
origin https://github.com/42folders/news-classifier.git (push)
```
[Other notes on git remote](https://www.git-tower.com/learn/git/commands/git-remote#:~:text=%2Dv,the%20remote's%20URLs%20in%20listings)

## **How do I remove a file from being tracked by git?**
```
> git rm --cached <path_to_file>
```
After that, do a commit and push. 

https://stackoverflow.com/questions/50034192/how-to-commit-changes-made-after-git-rm-cached#:~:text=No%20need%20for%20git%20add,commit%2Bpush%20will%20be%20enough.&text=If%20you%20don't%20want,don't%20want%20to%20push.


## **If I have renamed a file locally and then pushed it to the remote repo, I still see the original file in the remote repo. How do I get rid of that original?**

At this point, git status will reflect the original file has been deleted from the local repo.

I'll need to remove that original file from being tracked using git rm -- cached <orig_file_path> as well. Thereafter, commit and push. 


## **An editor window pops up, asking for my commit message. How do I enter text into it?** 
If forgot to type a commit message, an editor window ("vi") pops up asking for a commit message -- clicking with the mouse, enter, escape, delete keys don't do anything, and I have to go google...

It's comforting to know I'm not the only one who's been flustered by this: https://stackoverflow.com/questions/73012357/please-enter-a-commit-message-for-your-changes

To commit that to memory, I tell myself: 
**"I write and escape worq"**

I for insert,
write your comment
ESC to escape,
:wq to quit. 
