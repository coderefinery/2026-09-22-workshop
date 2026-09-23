+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 2"
+++

This document contains the shared notes activities, some direct identifiers have been removed.

# Day 2 - 23/09/2026

# CodeRefinery workshop temporary archive of the notes

# Day 2 

## Reminder: Install git

To follow along with everything we're doing today you'll need to set up [Git in the terminal](https://coderefinery.github.io/installation/git-in-terminal/#git-in-terminal).

## Icebreakers

### When you share code, how do you do it? (poll, vote with "o")
- Email: oooo
- USB Stick or similar:
- Online repository link (e.g. Github): oooooooooooo
- Online repository (git clone): oo
- Cloud storage (e.g. OneDrive, Google Docs, University Cloud): ooooo
- Screenshot: 
- Photo of a monitor: 
- Copy-paste to email/chat: oooo
- Direct file access on shared system: oooo
- HackMD or similar (pastebin also): o

Others, write below:
- [IPoAC](https://en.wikipedia.org/wiki/IP_over_Avian_Carriers)
    - :D


### What was the last animal you saw?
- Human primates: ooo
- Wasp (and I kindly let her way out)
- Dog: oo
- CATS
- my daughters
- my cats
- pigeon 
- .
- bird: o
- cat: oo
- cat
- beetlecity rabbit
- squirrel
- 

### What is some traditional food you make "wrong"?
- This is difficult, but my mom makes pasta carbonara wrong (sorry mom)
- Sushi
- Any chinese or japanese buffet in Finland :D
- pizza Grandiosa and the like
- i never get pizza right :,) 
- tiramisu without lady fingers and petit biscuits instead
- Stir fries
- paella that is not paella :')
- potatoes:))
- Finnish fish soup
- porrige
- Basil pesto with cashews instead of pine nuts
  - that's what a Genovese would do. Pine nuts are crazy expensive, and Genovese people are stingy (I'm from Genoa)
  - I didn't know that.
  - I am from Genoa too...belinone!
  
## Leftover questions from yesterday (or new ones in the morning)

- Some notes on the installation guide page for VS Code versus live installation on 23.9.2026:
    - current LIVE INSTALLATION does not have INSTRUCTION STEP 5 "5. Choosing the OpenSSH executable: “Use bundled OpenSSH” and click “Next”. "
AFTER STEP 4 live installation goes to > STEP 6 "Ensure that “Use the native Windows Secure Channel Library” (prob was deafult setting)
    - current LIVE INSTALLATION does not correspond to INSTRUCTION STEP 9: "Ensure that “Default (fast-forward or merge) is selected and click “Next”" the instruction step 9 did not EXIST in live installation: The live options were:
*Merge [default]
*Rebase
*Fast-forward only 

 
- Could you also please show how to delete old repositories in a Clean way, also the local copies to free space. The Deletion of the branches could be helpfull as well to see once again.
  - Deleting old repositories on your own computer: just delete the folder. Everything is stored only in a directory named `.git` in the folder itself - nothing else.  If you delete only `.git` then all history and "git stuff" is gone, and you are left with only the current versions of the files.
  - from GitHub, you can delete via settings
  - Deleting a branch on your own computer: `git branch -d BRANCHNAME` (or `-D` if it would lose commits)
    - with `-d`  git refuses to proceed if the branch has not been merged (and if you'd "lose" commits by deleting it, although in git it's very difficult to really lose commit)

- this is more of a Terminal question, but is there a way to save the history of all commands for a particular task, e.g., interacting with git, so that that history can be retrieved in later sessions?
    - You can see your terminal history with the command `history` and drop it in some file with `history > filename`. If you want to filter it only for git commands, then you could try some "clever" filtering like `history | grep "git" > filename` (here only retrieving those commands that include git). This is not perfect but it is one way.
    - As mentioned by the instructors, you can also hit the up arrow key to see previous commands if you just want to search for one command and use it right away. Hitting control+R on the terminal allows you to search your command history (at least on linux, if someone can confirm for MacOS and Windows).

- MacOSx Terminal uses zsh instead of bash. Will all git commands work fine?
    - yes

- who owns GitHub? Who owns the data uploaded on GitHub? Can the GitHub owners have access to our repos at any time?
    - Microsoft. They do not/cannot claim ownership of your data, they are more like a "processor" with whom you have a contract. And I am pretty sure github admins can access anything. I will find the right lines in the Terms of Service
        - "We treat the content of private repositories as confidential, and we only access it as described in Section E.3 below—for security purposes, to assist the repository owner with a support matter, to maintain the integrity of the Service, to comply with our legal obligations, if we have reason to believe the contents are in violation of the law, or with your consent."  https://docs.github.com/en/site-policy/github-terms/github-terms-of-service
    - There are valid GitHub alternatives, it's just that "everybody knows github"
    - Alternative ethical European online git remote option: https://codeberg.org/ (the "issue" is convincing your colleagues and collaborators to also switch to the same online tool, GitHub historically had already people there so even for us at CodeRefinery it is still the default option)
      - Note that codeberg has the option of "mirroring" a repository: you can have you main repo on codeberg and set it so that every time you push (or at least "periodically") another repo on github is updated.

- is there a way to include a repository in another? Imagine there is a library that is being developed separately. I want to include it in  another repository but be able to track the link and update it whenever needed.
  - It is possible to do it with [submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). But it gets complicated. I make mistakes with this often. If you are really keen on that, learn the submodule tool *quite* well
  - If you can adjust the question, one would package the library and install it separately.  For example, the way I use one Python package I develop in another project is to `pip install -e ../path_to_my_development_area/`.  If it's a finalized/published library, I can install it from the cloud directly.


- can you zoom in a bit? in shared classrooms this doc is quite hard to read. Thanks!
    - Thanks for letting us know. We will remind the person screensharing. Let me know if now it is better.


- would a submodule be the best way to set up developer environments in general? We will be working on developing an XML repository and need a safe setup for this. How should we proceed?
  - Let me see if I understand: you have a data repository that you would like to use as a submodule, or at least to reference from the code repository?
    - Rather: we have a data repository that will now undergo significant changes in both XML data  and need a setup for a developer environment that will keep them separate but also replace the old when the development is finalised. It also needs to be connected to a database instance.
      - Submodules are a way to "link" two repositories together. You get a many-to-one relationship between commits of the two repositories. Typically this is something you need if there is an existing repository, with its own life and use cases, and you need to use that in another repository *so that you can version-control them together*. If the two repositories do not exist yet, I'd say it's much simpler to have a single repository so you can version-control all you need in a single repo, which is quite simpler.
        - but does this give us a separated developerment enviroment? We will be doing a very complex makeover of all files and the encoding and fear there will be a risk to do it in one repository
            - If you only have one repository, you can use branches to create a development version of the initial state of your project (in your case, with the original data files) where you can make changes while still keeping the original files on the main branch. This is a pretty common practice to separate development from stable versions of software, for example, and of course you can have more than one development branch. You can also manage the permissions to control who can merge, if/how the merge can be done and so on, to make it safer.
            - That is one way, other way would be to create one repository with the original project and then fork it to create a new copy where you do all the changes (if you do not want both versions overlapping at all). This is a bit overengineered in my opinion if you are the owner of the original repository too, but it is another option.
            - Submodules are useful when you have different parts of a complex project doing very different things (so it makes sense to put them in different repositories), but then you want to reuse them (their functionalities) on a different repository.
        - Thanks, that was useful! Do you also know if it is possible to connect a branch to a separate database? We will need to do that in order to see the development in a published web version of the setup.
            - branches are different versions, potentially incompatible. If you are using different databases, or more in general, different configuration of your software, and your software should work with all the different configurations, *then* I'd argue that using different branches for this is not a good idea. The more branches/repos you have *on top* of the complexity of your code, the harder it is to work with it. Branches are a "necessary evil" when multiple people work on different things at the same time independently, but a lot of problems in the long run come from misusing this feature
                -   This is a really good point, it depends on how complex the project is or you expect it to be. If only one development version is needed and you'll work just on one new configuration, then it might be okay, but 100% true that taking it further would be misusing this and create more problems in the future. Summing up, it depends on the project a lot and most of the time there is no perfect solution for very complex projects (but hope the discussion above helped somehow)
                  - (I say this because when I started using git I thought that branches would map nicely to whatever situation I had with "multiple things", but this is not really true) +1
       
    

## Day 2 intro

## Cloning a Git repository and working locally
https://coderefinery.github.io/git-intro/local-workflow/

- Here is the shell tutorial, mentioned by the instructors in case anyone wants to check it later: https://www.youtube.com/watch?v=xbTTDLA3txI

- How we will proceed: open VS code?
    - For now enjoy the intro, then when there is the exercise you can choose if you want to use the Terminal, or VSCode, or RStudio (see the three tabs in the exercise at: https://coderefinery.github.io/git-intro/local-workflow/#solution-and-walk-through)

- What is preferrable: to use git bash or shell?
    - If you are familiar with Bash/Linux/Mac terminal, I would use gitbash (I assume you are on a Windows machine). The instructor is using Bash on Linux (but powershell commands also work with the commands the instrucotr is using)

- "Please make sure you have the correct access rights and the repository exists." Is this ok?
    - I assume you got that as the output of some command. Which command?
        - git clone git@github.com:cr-workshop-exercises/recipe-book.git
    - You get that error if you did not set up ssh keys with github, In the sub tab here https://coderefinery.github.io/git-intro/local-workflow/#cloning-a-repository you can pick "https" which is going to do a "read only" from the remote without checking your identity. The command is then: `git clone https://github.com/cr-workshop-exercises/recipe-book.git`
        - which command? i don't see any ssh command sorry
            - You can run this command `git clone https://github.com/cr-workshop-exercises/recipe-book.git`   - if you use `git clone git@github....` then git will use, under the hood, ssh.
            - If you use `git clone https:.//...`   then git will use https 

```
$ git clone git@github.com:cr-workshop-exercises/recipe-book.git
Cloning into 'recipe-book'...
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```
- what did i make wrong?
    - You get that error if you did not set up ssh keys with github, In the sub tab here https://coderefinery.github.io/git-intro/local-workflow/#cloning-a-repository  you can pick "https" which is going to do a "read only" from the remote without checking your identity. The command is then: `git clone https://github.com/cr-workshop-exercises/recipe-book.git`
    - For later: if you need help setting up your terminal with SSH authentication with github (this is needed if you want to "push" your local work to the remote at github.com) then you should follow the steps at  https://coderefinery.github.io/installation/ssh/#ssh and 
    - It is very uncomfortable to ipen so many windows, maybe you can make simply a list of commands (it s for future). Maybe i didn't follow what should be done-very quick for me
        - Thanks! We recommend keeping just these 3 windows https://github.com/coderefinery/workshop-intro/blob/master/livestream.md#practical-setup but of course it depends on what is going on on your computer, but we are happy to help anyway :) The zoom room from the morning is still open if you want to join there.
            - oh, no additional window with zoom. I have git and i only wanted to clone, why it does not work? which command should i make: 1_, 2 , 3 is it  bot possible to copy paste here?
                - This command in the terminal will work to clone "git clone htthttps://coderefinery.github.io/git-intro/local-workflow/#creating-branches-locally)ps://github.com/cr-workshop-exercises/recipe-book.git"
                    - I did it and then? seems it works
                        - Then continue with step 3 in the page we are at right now
                            - Receiving objects: 100% (239/239), 57.09 KiB | 11.42 MiB/s, done. Resolving deltas: 100% (90/90), done. it seems to work_ can you put the commend here, i am lost between so many windows.
                                - If you need extra help please join the zoom, otherwise it is more efficient to follow all the steps in our materials than me copy pasting them here https://coderefinery.github.io/git-intro/local-workflow/#creating-branches-locally
                                - It is not comforatbkle always to junp from window to window
                                    - I understand and agree, it is the best we can do :) 
                                    
- git switch --create another-recipe main fatal: invalid reference: main -that what i got
    - Please make sure you are inside the cloned repository. After the "git clone" command you need to enter the subfolder you copied locally with "cd recipe-book" 
    

- Just to mention that I use https and I was not prompted to write a password (sharing in case it helps someone)
    - With https you do not need to tell to the remote GitHub who you are, so it is ok for downloading a repository like in this case. But you will not be able tomorrow to "push" (send from local to remote) if you did not set up your ssh keys and clone the repository with ssh remote.
        - Great, thanks for clarifying!
    
- Is SSH like a password type thing belonging to your computer? because I have SSH set up and I also use it to log into my institutions HPC, which has nothing to do with GitHub.. i don't fully understand what it is?
    - Yes, in a way. It stands for 'secure shell protocol', it is a protocol used to communicated between two computers over an encrypted connection. So when you log into one of the HPC machines, for example, with an ssh and read/edit files, the data is transmitted via the encrypted connection
    - But SSH can also just be used as a way of transfering files securely.
    - The "private key" is an identity that you can use to prove who you are. Keep this safe. The public key authorizes you to different services. This means someone else can't push e.g. malware into your repository.

- I missed *where* on the github.com page you found the link git@github.com:cr-workshop-exercises/recipe-book.git
   - On the front page of the repository, there is a green button. Usually on the right side of the branch menu and the left side of the "About" title


- I created a branch named 'another-recipe', but I cannot see it with > ls 
   - `git branch` lists branches. `git branch -a` also lists branches from the upstream repository (the one on github) 
   - `ls` lists *files*. *branches* are a concept that only git knows about, and you have to use `git branch` to see them.

 - I am doing this in Rstudio, after clicking "create branch" there is an box for "remote" with "origin"and "none" as options, what are these and should I deselect Remote?
   - This makes the branch track a corresponding branch on GitHub. It becomes a "tracking branch" but it doesn't automatically keep in sync -- it just says which branch the commands `push` and `pull` work against by default. For this exercise we don't push or pull from GitHub after the initial `clone` so either value is fine.


- I am having issues with sound today - I logged on a little late so not sure if I have missed a message but I can't hear anything. I've checked I have sound via youtube which I do, and I have the volume up etc.. any ideas what might be causing this? Sorry!
    - Right now we are on an exercise break so no sounds :)
      - OK, thank you.. hopefully I will hear when you come back!

- I get this when I try to add a new file. What am I doing wrong?: $ git add new-file.md  fatal: pathspec 'new-file.md' did not match any files
     - it means Git can not find this `new-file.md` file in your current folder, try `ls` and check if you are in the right folder.

- I am working and usually work from command line. Usually after commiting i push and then open github to pr. When I try git merge branch_name in the terminal, it weirdly opens vs code and i dont know what to do with it?
   - VS Code is probably set as the default text editor for git. It's probably asking for a commit message for the merge. Saving and closing the file should be enough.
   - Yes that worked thank you!

- Partly stuck on point (5).
    - Which part?
        - for command "git commit -m "Short summary of the change", I get 
            ``` 
            Changes not staged for commit:
            (use "git add <file>..." to update what will be committed)
            (use "git restore <file>..." to discard changes in working directory)
                modified:   mixed-nuts.md

            no changes added to commit (use "git add" and/or "git commit -a")
            ``` 
           - Add the files using `git add filename`

- I did the excercise in VScode, now i wanted to do it with the CLI. It say there is not git repo. do I need to clone again even though I did it with VScode?
    - You need to first go in the right place of your computer where the repository is, e.g. "cd code/recipe-book"    
    - different folder then the project I set up for the course then?
        - Check where vscode is writing and go to the same place with the terminal so that you are in the same folder
        - from vscode, you have to "open folder" choosing the folder/directory where you cloned the repo/where the repo lives
        - found it thanks


- I have in my old git notes 'if you switch to check someones changes on another branch, it will overwrite your local branch - do not do this' is this true? 
    - Yes, if the changes are not committed (and you do `--force`, otherwise git will refuse to do it)
    - Committed changes are safe, they will stay in the history of the branch where you committed them. Uncommitted changes that do not conflict, they may stay in your working directory after switching branches
    - If you have an untracked local file that a git switch command would overwrite, you should get this error message and nothing will be lost
        ```
        error: The following untracked working tree files would be overwritten by checkout:
	        test1.txt
        Please move or remove them before you switch branches.
        Aborting
        ```

::: info
### Exercise until XX:45
https://coderefinery.github.io/git-intro/local-workflow/#exercise

I am
- done:ooooooooo0oo
- working on it:
- skipping it:
:::


- It might be good to mention when you're using linux specific commands like `ls` or `pwd` because these will not work for everyone. 
  - they work for everyone *who is using bash or zsh* (e.g., git bash on windows). Powershell has similar commands to bash (not many, but the most common). The "old" cmd prompt on windows is instead very different, this is true.
      - oooh okay i always work from miniforge and today im on windows. is there any benefit to changing to bash?
          - Good question... if you are used with cmd syntax, you can stay in "cmd" and remember the differences "ls in linux is dir in cmd etc". If it doesn't really matter, then switching to gitbash is more powerful since it is compatible across many platforms (linux, mac, supercomputers) and allows for powerful "scripting" (e.g. you can make sure your pipeline is fully scripted) (and powershell is a compromise between the two while staying in a full MicroSoft option)

- The info page and solution for VS Code https://coderefinery.github.io/git-intro/local-workflow/#solution-and-walk-through for cloning the repository in VS Code is pretty visual & selections from menus (similar to Github Desktop). Was the point not to use Terminal in VS Code? I mean the manually written git commands? Will the commands be same if I use VS Code -> Terminal  
    - Yes the main point is to use a graphical interface. Most likely the same exact commands are then run by VS code. I personally prefer the terminal to see what is going on, but it is a matter of tasts/habits.
        - but you dont use the VS Code Terminal but instead... the black window of the cmd or Powershell or whatever?
            - The vscode terminal is as good as any other terminal. (I use gitbash on windows, iTerm2 on mac, default bash terminal on linux)
                - ok, on Windows VS Code, can I mix and match: clone with the buttons/menus -> use these git commands in the VSCode terminal in between / instead? 
                    - Yes and it's the best way to learn :) Just make sure you are in the same folder (sometimes terminal folder drifts from the Explorer folder in vscode)
                        - how do I check in WIN VS code Terminal where I am. does pwd work there? gitstatus?  (hm, currently, it seems to offer that information in the terminal command line but i've not done much yet)
                            - "Dir" also tells the folder where you are right now. At least in my windows cmd I see the full path in the prompt itself. If your terminal is powershell or bash, then "pwd" works. (my vscode on windows, default installation has powershell has terminal so "pwd" is what you want to run)
                            - yes, VS Code Terminal shows powershell currently, so pwd ok. However, at one point it read git. So need to be aware that what I write, perhaps there are commands that powershell understands, git doesnt? 
                            - Q?: is  this current pwd path the place where the Clone repo -button will clone the repo folder? -> I can here point it to a subfolder? 
                                - Good question. I test it. So the answer seems to be yes. After I clone the repo with vscode, the terminal is by default inside the repo I cloned. If I want to go into a different folder then I use cd in the terminal or from explorer "right click -> Open in Integrated Terminal".
                                - So I need to first navigate the Terminal to show the correct path -> then Clone Repo -> then it gets cloend there?
                                    - I am not sure about that... I can try. :) For my it went there automatically if I first clone and then open the terminal.
                                    - Thanks. What Iam trying to do here is to make sure the repo gets cloned to eg. Folder1/Subfolder2/CLONEFOLDER, and currently (before Cloning) the vs code terminal > says (eg) Folder1 (I am now assuming the clone folder would becoma Folder1/CLONEFOLDER)
                                        - My test: I am in a different folder in the terminal. I clone a new repository and with GUI I ask to save it into a completely different place. THen it asks "Would you like to open the repository or add it to the current workspace?". I said "add to workspace", now in the explorer I see it, but the terminal path did not change. So in the explorer I right click and then "Open in integrated terminal" and it starts a new terminal in the right folder.
                                            - I will try this after break, thanks.

- Can you show how to create new file on Vs code? I already created a new branch. I couldn't use the current instructions as the UX/ UI of VS code has changed
  - if you using the VScode, you can eighter use the terminal in the vscode and use same commands, or open explorer in the left side , find your project, and click the "new file" icon.
  
- what is the output of command+"^C"?
    - If you press Ctrl+C it's usual result is to interrupt or cancel the currently running command. So you would see `^C` and then a new empty prompt line after (`$` in bash). Is that what you mean?
        - Yes, why is it included in the commands atm?
            - I actually missed that completely, could you let me know where it is? (If it was in the live demo, the instructor probably cancelled the command to do something else or there was a typo, or something similar.)

- In VS Code: what is the difference between left hand bar Expolorer and Source Control. Both allow Clone Repository.
    - The Explorer is a file explorer and the source control has a "git" perspective on it. I don't see how to clone a repository while in the Explorer view in my VScode (Windows).
        - I just open VS Code, and  explorer in the left hand, options: No folder opened > You nave not yet opened a folder "open folder" [blue button] and You can clone a repo "Clone repo" [blue button]. Same buttons exist in Source Control, less helptext there. (I'm logged in VS Code with a github user)

- what's the difference bewtween git switch and git checkout? thanks!
  - git checkout does many things. It can be used to *switch branches*, or to "checkout" files to a particular version. It's kind of confusing to some people. Somewhat recently, two commands that have a smaller scope were introduced: *switch* and *restore*. Switch is used with branches, *restore* with files. 

- What is the difference between committing and stashing? I have tried to switch branch without committing which does not work. Copilot has then suggested to stash.
  - stashing and committing have a similar mechanics, but stashing does not happen on a branch. 
    The idea is that you `stash` when you don't want to make a real commit, but then you `stash pop` to get your changes back, which amounts to a merge (and you can have conflicts when you do `stash pop`). But I don't want to scare you: `stash` + `stash pop` is a very convenient way to circumvent the limitations e.g. that you can't pull while you have uncommitted changes. But remember to `stash pop` if you still want to keep the work you `stash`ed away before.

- In the exercises we merged our branch to main in terminal. Why? wouldn't you usually push and then merge later? Whats the diff?
    - We wanted to practice merging locally :) But also, later we will see conflicts, and they are often easier to handle locally.

- Is it possible to create a branch locally and later push it to the repository so it is also a branch in the remote repo?
    - Yes, it is. When working local everything is just local and later you can decide what should go to remote.


::: warning
### Break until XX:20
:::


## Command line, GitHub/GitLab, and VS Code

https://coderefinery.github.io/git-intro/archaeology/#command-line-github-gitlab-and-vs-code

- Could you please copy paste this directory
    - sorry, which directory do you mean? 
    - the one which you clone now
        - This one: https://github.com/networkx/networkx
    - https://github???
    - You can find it also in the materials: https://coderefinery.github.io/git-intro/archaeology/#searching-text-patterns-in-the-repository
    - so long to find, i want to follow
    - Could you please just copy paste
        - yes, it is the first link I copied above :)
        - https://github.com/networkx/networkx
        - They were cloning that repo
        
- I missed the command to show the commit history. What was it? Perfect. Thank you.
  - `git log` will show the commit history.
 
- when to use annotate vs blame?
  - `annotate` is a more neutrally-named version of the same command.
     From the main page of `git-annotate`
     > The  only  difference  between this command and git-blame(1) is that they use slightly different output formats, and this command exists only for backward compatibility to support existing scripts, and provide a more familiar command name for people
     coming from other SCM systems.


- FYI, when the text fills the terminal, there is not enough time to see what the command was. 1 second pause would be apprecaited.+1
  - thank you for pointing this out!
  - Yes thanks -- I'll try to remember this!

- In VSCode RUff is flagging "Error while resolving settings from workspace" ... please refer to logs for more detail. When I am switching branches -> Using Terminal within VSCode
    - This seems to be quite specific to your extensions. My guess is that different branches might have different ruff settings and that is conflicting when switching (maybe you changed something in the toml file or other local files witout committing?)
    - Or incompatibility between the repository's configuration and your language server
    - Feel free to paste some of the log here if you want to know for sure


- When cloning my own forked version, the SSH option in Github says "You don't have any public SSH keys in your GitHub account. You can add a new public key, or try cloning this repository via HTTPS." Was there a guide page forthis? 
  - https://coderefinery.github.io/installation/ssh/#ssh


::: info
### Exercise until XX:05
https://coderefinery.github.io/git-intro/archaeology/#exercise

I am
- done: oo
- working on it:
- skipping it:

:::

 - why?
    ``` 
    ""$ git checkout -b exercise networkx-2.6.3
    fatal: a branch named 'exercise' already exists"
    ``` 
    - The branch has already been created. This happens if you run the command twice, for example. You can see what branches exist with `git branch`
         - ok , thanks
- I am working in the just-before branch. I get an error with git bissect good f0ea950. The error is: Bad rev input: f0ea950
    - We'll demonstrate git bisect after lunch
  what commit exists in the [git-bisect-exercise](https://github.com/coderefinery/git-bisect-exercise) repository

- why do we need to create branches locally? Could we not just edit in main and then push to github?
    - You can do that, but it depends on several things. If you are collaborating with more people, it might be good to have your own branch and only merge it back through a PR. Especially for big or complex projects, it usually helps to avoid conflicts.
    - Also, it depends on how long it will take you to make your changes. If you just need to make small fixes, editing the main and pulling on the same session can be an option. But if you are developing something or adding big modifications (changing some functionality in your code for example), it might take you more time to have it ready. Having a branch for developing it allows you to test it without affecting the main branch of your project (so you can keep using it even if you break the code in the development branch).
    - That said, creating branches is easily overused and it can create problems later. We will talk about good practices in the next lessons where we will touch this issue.
        - actually, we will talk about this later today :D
    - Niche but maybe not anymore niche case: I create and switch to a new branch when I want to let an AI agent code on a task. Then look at the changes and later decide if it should all gone to the bin or some things merged back to main. So the collaborator is the AI agent and I can decide if what they did is good for going back to main. :+1:
      - Even at OpenAI official trainings they recommend using worktrees (i.e., branch AND separate directory actually "served" from the same repository)
          - the word "worktree" triggered a memory that I've read about this (no personal experience, yet) and people having (obvs) some difficulties; definitely need to learn about this since it's going to happen and better make it happen as safely as possible - Irealize this is not on the current day's plate but just in case anyone else is wondering, here's a link - the multitude of terminology around the same concepts is quite something (link: if permitted, if not - instructors please delete https://learn.chatgpt.com/docs/environments/git-worktrees) :+1:



::: info
### Lunch untill XX:00
:::

- Is there etiquette regarding how much to change on a single branch? I've been told before to do many small prs rather than one big one. 
    - Not really a general recommendation. Bigger projects will have their own culture. I like to have one PR address one bug, problem or development goal.
    - You can make "development goals" big or small (by splitting big ones into smaller ones). The "Agile" movement suggests to prefer "small" goals that can be integrated often. There is some evidence that this approach works better, for various reasons... 

- Comment: `rm -rf .git` is something you want to do *very* rarely

- Blue on black is pretty hard to read! yes, i also think so
    - Yes, much clearer now!

### After Lunch ice breaker: What is your favourite color scheme? 
- All I see is The Matrix:ooooooo
- Dark mode: oooo (doesn't it save energy?)
    - other: Solarized dark (Solarized is supposed to be easy on the eyes): ooo
        - this one is great if you have headaches or migraines triggered by screen light :)
- Light mode: o
- those ones where all the colours mean something helpful o
- dracula
- Monokai Vibrant

## Questions, continued

- please give the link to repositry
    - https://github.com/coderefinery/git-bisect-exercise
    - link to the exercise: https://coderefinery.github.io/git-intro/archaeology/#optional-exercise-git-bisect

- While trying to check a particular commit, do we need to create a separate branch to execute code corresponding to that commit? or can we execute an old version without creating a branch?
  - you do not need to create a branch to do anything that is not git-related. You might want to create a branch if you intend later to modify the code at that commit and do another commit, for example
- How did you find commit 1 without scrolling through hundreds of commits from `git log`?
  - you can use 'pgdown', or you can search in that interface by typing `/` followed by `commit number 1`. In general, search is a good feature to know (all "pagers" thingies on the command line use it, for example man pages and "less" output) but for the time being you can just "speed scroll" using pgdown, perhaps?
      - Yes, searching combined with pgdown turned out to be efficient.

- how does bisect work in practise when you're not working with a single file which outputs a single value? Just more testing between bisect commands?
  - you should in principle still get to a commit that "broke" your code. If you can't automate the "bad/good" decision, you need to do it on your own manually (no "git bisect run")
  - In practice you also need to consider that you'd like your code to work at every commit, otherwise the decision on whether the code is in a "good" or "bad" state will be harder to take
  - If you're not sure e.g. the commit is broken for some other reason that's not of interest to you can run `git bisect skip`
    - But this is annoying so this is one reason why people often keep a clean commit history without broken commits


::: info
### Exercise until XX:00
https://coderefinery.github.io/git-intro/sharing/#exercise

I am
- done: ooo
- working on it:o
- skipping it:

:::


- Win VS Code. Created local folder Y -> trying to get Y into Github. 
  My local folder structure: User/XX/Y --> Win VS Code -> Explorer -> Open folder -> Y 
  VS Code asks: Do you trust the authors of the files in this folder? 
  Options: Trust the authors of all files in the parent folder XX. / Do not trust. 
  [Why does it ask to trust XX, why not Y]
    - side note: having used Github Desktop (no terminal there, so menu based like VS Code so far, it seems a bit more .. clear than VS Code; pros / cons if you have any are welcome! )
    - I'd reformat a bit the question if you don't mind... (I can do it for you if you allow me!) / sry, psated from notebook and it frist created several bullets so a long read was better than that
       - bullets are good, you described very well your problem!
           it looked like 10 beginnings of separate questions, should have done indents, not time
       - We are actually secretly practicing the "How to document your research code lesson", when we will see about markdown syntax :-) 
    - I think that the problem is that VSCode might be exploited to do malicious things when it opens a directory, so by default it opens it in "restricted mode". Version control AFAIK does not work in restricted mode (I don't exactly know why). May it be related to AI agent security? I don't know
      - e.g. a language server (which e.g. has code completions, shows docstrings and jump to definition) might do all sort of things in response to configuration files in a repository including arbitrary code execution (i.e. can do anything on your machine)
        - yes i think so too, since when I read further on the read more, the VS code info says this particular setting (trust) will be used by ai agents as well 
    - ok but still dont get why it wants to trust the parent folder XX (and do stuff to it, apparently) and not just the actual folder Y 

- I get an error:
    ``` 
    git push -u origin main
      error: src refspec main does not match any
      error: failed to push some refs to 'https://github.com/...
    ``` 
    - The error is telling you that Git cannot find a local branch 'main'. Can you check if your branch is called main and not master? 
    - Also, please check that you do have initial commits
    - Thanks, worked now. Committing was ply the issue
        - Good! :)


::: info
### Break until XX:10
:::

- If you did `git add .` does this also add those in subdirectories? 
  - yes, except files ignored by `.gitignore`.
- inside the repository, how to get the 'origin' address?
  - `git remote -v`
 
- What is the difference between `git pull` and `git pull origin main`?
  - `git pull` will use the configured fetch tracking branch
  - while `git pull origin main` explicitly pull from `main` branch

 
## Practical Advice
https://coderefinery.github.io/git-intro/level/#working-on-the-command-line-use-git-status-all-the-time


- What is the difference between "commit" and "push"
    - "commit": tell your local repository to take a snapshot of what is known to git (i.e. added with git add)
        - extra comment: when you commit, you can attach a (short/long) comment to that snapshot, giving some context to the changes that happened compared to previous commits. This is pretty useful when used properly, giving you a meaningful git history of your changes.
    - "push": send all the most recent snapshots (everything since last push) to a remote repository
    - There used to be other Version Control Systems where "Add-Commit-Push" was a single command, it feels kind of natural that way. So it's normal to get a little disoriented

- So it is good to commit and push?
    - well depends on your workflow and how small chunks you want to be able to use to do things like bisect, track what is changing, etc.
    - a commit is one chunk of work(ideally, for me usually it is what I did before I had to stop for some reason ^^), with push it gets saved to a remote location
        - to add on this, you could create several commits locally without pushing. Once you push, then you'll save all of them in the remote location. It is good to remember to push at some point though :)

- .when we commit from one branch all changes comes from this branch or from other branches as well?
    - from one branch, if you change branches, you need to either commit the changes you made to that branch, or decide to stash or discard them. Stash meaning that it is not commited, but git can retrieve it for you, discard meaning that the changes are going to be gone for good.
        - Thanks a lot!


- How to remove something from a commit that I no longer want added?
    - You can but it's risky! `git rebase -i HEAD~n` where n is how many commits to look 
    - On new versions of Git you can do some "history rewriting" with the `git history` command, in particular `git history fixup` is a way to commit your staged changes to a *previous* commit
    - `git rm --cached name-of-file` can remove it from Git, but not your computer


## What to avoid
https://coderefinery.github.io/git-intro/what-to-avoid/

- so basically create an "output" folder into repo/project and .gitignore that? and just output images/pdfs and generated stuff into that? 
    - That is a good strategy, I personally keep the "input" and "output" folders in .gitignore
        - yes, like the "data" folder = input



## Feedback for Day 2 of CodeRefinery workshop

:::success
- Today, we covered everything in the schedule: We moved from the GitHub web interface to local computer and experienced the power of working locally, Inspecting history, Sharing work, Practical advice, What to avoid.
- Day 3 is when we will collaborate together, if you are following alone, you can be a collaborator in the exercise
- If you are planning to do the collaboration exercise tomorrow and are not part of team, please open an issue at https://github.com/cr-workshop-exercises/access-requests/issues/new?template=access-request.md (you don't have to write or edit the text there, just click the green 'Create' button).
- For day 3, If you plan to do the exercises please make sure you have a working git installation in your computer (e.g. with VS Code or with the shell terminal, see instructions at https://coderefinery.github.io/installation/) AND with ssh keys setup with your GitHub account

Twitch will store this video for 7 days, and hopefully it will be on YouTube by the time that expires.
:::

### Today was (vote for all that apply):
too fast: oooo
too slow:
right speed:oooooo
too slow sometimes, too fast other times: o
mostly right speed, occasionally too fast: oo
mostly right speed, occasionally too slow: o
too advanced:oooo
too basic:
right level:ooooo
I will use what I learned today: ooooooooooo
I would recommend today to others:ooooooooo
I would not recommend today to others: 


### One good thing about today:
- pretty good juggling given there are multiple methods cli, vs code etc +1
- i learned some new tricks using command line
- many practical tips for the actual work and good demonstrations
- i learned a lot and its fantastic with this note document, I can get answers to questions quickly and without shame :) +3
- immediate responses here were really helpful and insightful +2
- my questions were answered 
- I have learned git mostly by figuring things out myself (and by asking an LLM). Attending this workshop is very helpful regarding clarifying confusing things about git. 

### One thing to improve for next time:
- the workflows are quite clear, the first steps/env is always the thing that seems the wall (the things that will be obvious in a few weeks) 
- very lovely walkthrough a bit dense and fast through all the history discovery though :)
- a little bit slower



### Any other feedback? General questions?
- If we could still have a Zoom in the morning?
- Where should we write our gitHub information?
    - You can find instructions in the email you have recieved today (title: *"[Indico] [CodeRefinery-0926] Getting ready for day 2!"*). In the middle-ish there is a section called *"Day 3 for individual learners"* which describes how to proceed
    - and the important link is this: open an issue at https://github.com/cr-workshop-exercises/access-requests/issues/new?template=access-request.md 
