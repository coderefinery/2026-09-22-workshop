+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 3"
+++

This document contains the shared notes activities, some direct identifiers have been removed.

# Day 3 - 24/9/2026
### Icebreakers

### What is the largest collaborative project you've been involved with? (what's the project?)
(doesn't have to be work/technical)

- about a hundred people
- Weighted by how many people I actually work with, perhaps CodeRefinery itself...
- 20
- Company projects, so hundreds, even more, and a lot of sw development braches, but not with Git.
- for me it was like 6-7 people
- I guess it depends on how we define "project", a bit project can have many small subprojects 
- Also hundreds for large-scale research across many universities.
- About 10 people from three differents universities in Germany


### What secret guideline would you teach someone who joined your team now?
- Here is the onboarding doc where *everything* is explained and *everyone* is adhering to :P
  - and the link gives error 400
- Nobody writes bugless code.
- Just ask people when you're confused, there is someone that knows about everything and it will be faster than figuring out our systems alone. 
- You think you are here as a programmer, actually communication is the hardest part you do. +1!
- 




### Any other feedback? General questions?
- If we could still have a Zoom in the morning?
    - I think I got my problem fixed. 
    - Great!
- What are the Git commands that are needed to get the same info as the usethis::git_sitrep() in R?
    - In the R I used command usethis::git_sitrep() and that seemed to give information about the 
        ── Git global (user) 
        ── GitHub (user) 
        They had different usernames, and that was messing thing up.
    - Yes, I had 2 user names. One old. Both in GitHub. I guess one was using SSH and one HTTPS.
        - Note that all Github SSH connections use "git@github.com" as the SSH user (it uses your SSH key to figure out who you are).  Not sure if this is relevant.
            -Yes, the other was configured for SSH and the other for https.
            -Perhaps the other origin was on SSH and the other for HTTPS. Removed the other (https), and now only on SSH.
                This is in use now
                $ git remote -v
                origin  git@github.com:[username]...
            
- Where should we write our gitHub information?
    - You can find instructions in the email you have recieved today (title: *"[Indico] [CodeRefinery-0926] Getting ready for day 2!"*). In the middle-ish there is a section called *"Day 3 for individual learners"* which describes how to proceed
    - and the important link is this: open an issue at https://github.com/cr-workshop-exercises/access-requests/issues/new?template=access-request.md 
    - havent receceived a mail until now

- Comment: Sorry about the audio, now (since 10:52) you should be hearing everybody. Is the sound level okay? Can you hear everybody clearly? Please write here in the notes any issues you see with the streaming too and we will take care of them :)

- What to do next when we add the accounts?
    - You will get an invitation via email, you should accept the invitation (big green Join @cr-workshop-exercises button in that email)
    - Check your spam folder just in case (it is the email address associated to your github account)
        - Yes, i did , what next?
            - Nothing for now, you will use it for the exercises
            

## Git collaborative
https://coderefinery.github.io/git-collaborative/

- what is the difference between cloning and forking?
    - They are saying it now, but basically fork happens "in the cloud" (= the GitHub website), clone happens in your computer. The advantage of fork is that you now have a remote copy of the original repository under your name, so you can then clone the fork locally and do your new work on top of the repository that you forked. 

- what should we do cloning or forking?
  As far as i understand forking is possible if the repositoiry is public
  - clone if you want the repo on your computer.
  - fork if you want your own copy of the repo on the "cloud" (e.g., github.com)
  - fork and clone your forked repo if you want to have your copy on the cloud and want to be able to push/pull from it from your computer
      - Ok, understand,thanks
 - where is the template?
     - you don't need to do it for this exercise unless you are going to build your team (e.g. in a room that is watching the stream)
    - (Only needed for teams!) https://github.com/coderefinery/recipe-book-template
     
:::warning
Please accept the invitation to join the cr-workshop-exercise repository. It is in your mailbox.

(This applies if you opened an issue to access the cr-workshop-exercise organization on github. We can't give you access, we can send you an invitation that you have to accept)

We still have **7** invitations pending! One of these might be **you**!
::: 

- But i am there and see all the participants
  
- I am in the list :100: 

-  I am in template what should i do? 
   - If you want to create a repository from it, you can click on the green button "Use this template" to do it 
   - But this is only for the "classroom coordinators", or for whomever wants to own the repository that people will be invited to and collaborate with.
      - I want to do
      - I just created the repositiry
 
::: info
### Exercise until XX:10

https://coderefinery.github.io/git-collaborative/same-repository/#exercise

I am
- done: oo
- working on it:
- skipping it:
:::

- And if we have some conflicts?
  - they need to be solved manually 
- i have reated new branch and commited. do you see my commit? ***7**?
  - on which repository? On which branch?
  - did you create an issue too?
  - We can work on 2 repositories:
    - https://github.com/cr-workshop-exercises/centralized-workflow-exercise
    - https://github.com/cr-workshop-exercises/centralized-workflow-exercise-recorded
    Are you working in any one of these two repositories? If not, we likely can't see your commits.
    Also, if you are working on the terminal, you need to push your commit for us to see it remotely. If you are working on Github this is not needed.

- I see that i have commit and how can i do pull request?
    - About how to create PR: see section 5 on the exercise page, please (https://coderefinery.github.io/git-collaborative/same-repository/#open-a-pull-request-towards-the-main-branch)
    - And the instructors are demonstraiting right now :)

- I made pull request i await of approval, what should i do? :100:
  - we will review it now!

- Should i merge it to main branch?
  - you can create a PR first 
  - I did 

- I have commited from my branch, then i suppouse it should be merged to the main branch, right?
    - You need to create a pull request now, and we will review it, approve it and then it will be merged.

- Do you see my branch?
    - What is the name of the branch? You can see all the branches if you go to the main page ('Code') on gihub in the centralized-workflow-exercise repository, and click on the *'Branches'* button (right under the name of the repository, between current dispayed branch name and the *'Tags'*)
    - The branch is xxxxxxx
        - yes, it is there, but follow the instructions above to double check yourself :)
            - yes i saw other branches from xxxxx
            - but why don't you see my branch? I wonder why i am invisible, in my status is awaiting of approval of my pull request
                - what is your branch name? are you working on a fork repository instead or on one of the repositories linked above?
                    - xxxxxx is my branch name
                        - we can see it, you are fine :)
                 
                
- yes i follow the template, created the branch, change the strawberries make commit and pull request
    - yes, I can see your PR
    - while you wait for your PR to get approved, you can review other people's PR (add some comment, suggest changes)
    
- i see the commits 
    - +1

- do you see my pull request?
    - I guess yes? Do you see it?

- do you have recommendation for a GH template (what should be included etc?)
    - In general, I think this depends on the goal and the repository you are working with. When a project is very big, they might want to have certain templates for different contributions. It might include a checklist to help authors see quickly whether the pull request adresses a bug, feature, or something else, or whether necessary tests were done, for example. You can find some good examples if you look up one of the bigger projects on github. (examples: https://github.com/pandas-dev/pandas/blob/main/.github/PULL_REQUEST_TEMPLATE.md or https://github.com/huggingface/transformers/blob/main/.github/PULL_REQUEST_TEMPLATE.md)

- i see three pull request and mine is among them
  - please check this, it is not possible that you don't see my pull request
  - Could it be about the recorded vs non-recorded repository?
  - Are you the same person asking above or a new one? 
      - If the one above, please check our answers above :)
      - If you have a different branch/PR, tell us which one
   - please Review somebody else’s pull request and give constructive feedback :)
 
- I have reviewed someone's pull request and i think it merged? or not?
- How can we solve the conflicts? will we do that?
    - We will ignore that for now and discuss it after the exercise :)
    - More broadly: if this would be a research group, hopefully the two developers talk with each other and agree on which version should be kept. Sometimes conflicts can just be about trivial things though (e.g. some formatting changes). A code reviewer / manager could decide when reviewing the pull request.

- May i merge pull request of somebody?
    - please do
    - in this exercise we are all colleagues of the same team/group/company so we can merge each other's work.
    - It is nice <3

- One can consider the conflict for example i change to 2 strawberries, and someone the same to 3, what could be done then?
    - In industry a manager would decide :) You need to agree on which version to keep and then solve the conflicts and keep the final version.

- Solving the conflicts is very imposrtant +1

- how to create a pull request from command line and connect it to the issue?
    - There are different GitHub command line interfaces, https://cli.github.com/ is the main "official" one
    - There are probably more programs that can do it, too
    - Connecting to the issue, add the `#NNN` text to the commit title or  message somewhere and it automatically finds it.
        - `#NNN` being the number of the issue? (i.e. #12)


- If you are a member of only the org, but not the exercise team you will not have the option to create a branch. If that's the case, open a new issue just as before and we will make sure you are added the the team.
    - I have tried to review everyone in the organization and not the team and add them.  Still make an issue if needed

- When I review someone elses PR, should I always leave a message? Or is it okay to sometimes approve without a message?
    - I think it is always good to write something like LGTM 
    - Classic internet git joke "PR with 4000 lines of code", reviewer writes LGTM (looks good to me). PR with one line of code -> long comment by the reviewer
        - Heh.
    - Really, talk with your team and see what you'd like to do.


- When I review a PR that makes many changes, how deeply should I check that everything works? Do I more check there's no weird dependencies and the code runs, or should I also comb it line for line checking that all the logic is perfect? Sometimes I get asked to review code where I don't know what it does that intimately...
    - Very good question. Ideally people working together could agree on PRs that are changing only one or few things at a time. Like in an experiment where you don't want to change all parameters at once. But sometimes people do lots of work and commit and then just at the end of the day do a PR and the reviewer has to reconstruct all the history of changes and understand what is going on...
    - And really it's a human question.  Does your team want stuff reviewed?  Or even reviewable?  You can decide it's not reviewed, at the cost of not being reviewed.

- A bit out of topic but do you let a coding agent to do committs and pull requests on your behalf?
  - maybe you can consider joining our "Responsible use of generative AI in assisted coding" session next week, we talk about this there :) :+1:
  - I personally don't like it and try to tell the agent to never git commit or push :+1: 
  - I always want to commit myself.

- I was working locally and now do not know how to create the pull request
    - make sure you are in the right branch and commit and git push. The remote will be towards the same branch (git will tell you about this if it is not) and then after git push it will give you the link to create a pull request. Open the github link and then follow the page on github.com
    - get error 'remote: - Changes must be made through a pull request.
To https://github.com/cr-workshop-exercises/centralized-workflow-exercise
   ```
    ! [remote rejected] main -> main (protected branch hook    declined)
   error: failed to push some refs to 'https://github.com/cr-workshop-exercises/centralized-workflow-exercise'
   ```
   - Easiest way to fix this (in my opinion):
     - on  your computer:
       - create a new branch on top of your "main" branch, and switch to it:
         ```
         git switch -c <my-new-branch>
         ```
       - Then push the new branch:
         ```
         git push origin <my-new-branch>
         ```
       Now you can do all following steps on gitHub
     - On the github interface, you should be able to see the branch you just created and pushed
     - You should be able to create a PR from that branch
 

- I have merged someones PR, however the branch merged stright into the main directory, rather than under a subsection of a recipe. How would one go about fixing the folder/repo structures then?
    - One way: go back in time (the previous state) and basically undo the merge. We have an optional episode on that: https://coderefinery.github.io/git-intro/recovering/ - thanks 
    - another option is: create a new issue, fix it in a new branch and make a new PR
    - A small clarification about the issue: the problem was that the PR added *a file* in the *root* directory of the repository instead of a subdirectory (category).

- What if you have entered the wrong issue number (which is existing)in the PR? Is the other issue just closed by chance?
  - yes, but you still can reopen the wrong issue manually, and close the right issue manually
  - if the issue does not merge, you can edit the description and replace the issue number. or if it merged and closed you can reopen that manually.

- just to clarify, one cant do an PR from the CLI? Just on GH or VScode etc.?
    - there is also a "github-cli" that you can install to interface with github, but this is a *github* feature, not part of *git* itself
    - In general you would do these things on Github, though
    - You could also use a GitHub extension for VS Code and create a PR using that, but I agree with statement above - for me it is more intuitive to do it on the GitHub web  

- Just made a new Issue xxxx - how to make a branch from the Issue in Main, or am I missing something?
    - If you go to the main page of the repo (top left, "code" button), where it says "main", you can start typing a name for a new branch. If that name is not taken already, a button to create a branch with that name should appear.
    - When I select Brances there is no Button for that. 
    https://github.com/cr-workshop-exercises/centralized-workflow-exercise-recorded/branches
        - Are you sure you are in the team? 
        - Hopefully, as I could create issues?
            - I think anyone can open issues on a public repo. In the above link, can you see your github handle in the list? I could not see that members page,  but I got mail to join. Joined now. I'll re-try. MIne was "Closed #xxxx as completed." So I did not expected an other acceptance.
                - We closed the issue, when we sent the invite, you do still need to accept it. The account from #xxxxx I can see in the list now.
                    - There are still a few invites pending.
                    


:::info
### Exercise until XX:55
https://coderefinery.github.io/git-collaborative/code-review/#exercise
:::

- **Comment: please check others' PRs and add comments or suggestions!**
- **Comment: Remember to check back your PR in case there are comments or reviews that require your attention (your branch might be ready to merge)**

- Are people notified that they need to review?
    - In principle, if they have not muted notifications (as we suggested at the beginning)
- I previously did a draft pull request. Now i made a new branch and did the exercise where i made changes with typos and mistakes. I applied suggestions for the typo, and then did git pull and changed the bigger mistake. now when i pushed, my change from the draft pull request is also there... why?
  - If you apply the suggestions, you create a new commit on the branch of the PR. Then when you pull,  you get those changes too on your machine
  - but why did it pull an unmerged draft pull request that i made on another branch? and then it added it into the commit but maybes thats cuz i use add . 
    - did you switch to the main branch before creating the new branch?
    - you can also check the graph of commits to understand if the commit you made when applying the suggestions is there (`git log --graph --oneline --decorate --all` is the command I use for this, better to use an alias - it's also somewhere in the lesson material)
    - I did not switch back to main :) i don't fully understand what im seeing in the graph, but I bet I branched from my draft_PR branch! t
    
- what does it mean : close issue and how to reopen it 
  - if you click on an issue and go to the bottom of the page you *could* close the issue "manually" (but you can get it closed automatically with a PR or a commit, as we have seen)
  - To reopen it: you need to go to the list of issues, select the *closed* ones (by default you get the *open* ones), click on the issue you want to reopen, scroll to the bottom and you should have a button "reopen issue"



:::info
### Lunch Break until XX:00
:::

- Could you please, show in which case one should close issue, what does it mean and how to reopen it again?
    - sure
    - hope you saw it now on the streaming, let us know if the explanation was not clear enough
    - note that closed issues are not shown by default in the "issue" tab of the github GUI

- but in my case it was no button to reopen
  - could it be that you are viewing the PR instead of the issue? (just asking because otherwise I can't imagine a possible reason) 

- So that means i have no rights?
  - I will check if there is anyone not having rights and report back to you
    - it is funny, i can close but i can not reopen?
    - I have checked, all members of the cr-workshop-exercises organisation have write access now. 
    - Note that PRs can be closed but cannot be reopened (that's why I'm suggesting maybe it's a PR)
    - Which issue are we talking about? On which repository?
- Will I get a warning if I forget to sync my fork before opening a pull request towards the upstream repository?
  - on the github page of your fork, if you fork is behind then you get a message and a suggestiong to "sync" your fork. 


- Could you please tell exactly the sequence_ first create new branch in your repository and then fork it?
    - the instructors are answering this now
    - First, fork the repository. Second, create a branch on your own fork (instead of the original repository).
    - Does that clarifies it or do you need more instructions after that?

- after forking and returned to initial repository i lost my github
    - do you mean you got logged off? 
    - yes, it is dissppeared in my window
        - let's go step by step and see if there is something wrong or just a mix up of steps
        - can you try logging in again?
    - i am confused with your explanations
    -  very quickly andyou lost participant with such a manner
    -  I think you make some explanation and then wait a little bit when people will repeat, that will be cleare
    -  And you speak and speak and i didnÄt follow
          -  I understand, we will give some time for this exercise (now, if I am not mistaken)
    - the screen is b luerred, nothing is seen
    - With the gear icon, can you change it to source quality?
        - If the screen is blurred: you need to set the stream quality to "source". You can do that by exiting "theatre mode" and clicking on the settings "cog"

    - if you want, we can go through it again. Just let us know where you got stuck.

## How to contribute changes to repositories that belong to others

https://coderefinery.github.io/git-collaborative/forking-workflow/#how-to-contribute-changes-to-repositories-that-belong-to-others


- Git related - but not course related question. Since I added testing and pre-commit hooks my python project is blocked from commiting as the Smart app center (SAC) from Windows is blocking it. As far as I understood pytest and pre-commit are running small helper .exe, that are blocked. Anyway do tackle this without switching the SAC off? Hardware is company owned, so I cant change to much :/ 
  - I have limited experience with Windows, but these kinds of restrictions sometimes can be circumvented by running the commands via powershell (not even necessarily with admin roles). I'm not sure this fixes it - have you tried that?
      - you are a gem!!!!!!!!!!!!!!!!!!!! Stuck with the problem for over a week now. CLI comitting/pushing worked. Thanks a lot <3
        - Happy to have helped. And remember: with great powers (the CLI) comes great responsibility :-)
            - I simply never type 'rm', right? :P
            - In a git repository, you can. Git is a forgive machine (heh... well, not .git unless it's pushed...)
              - to remove .git you need `rm` but also `-r` and `-f`, it needs to be a *very* deliberate action
  - In the end sometimes you need to talk to the IT admins at your company... since they set the policy and make exceptions.  (That's assuming they even want to help you in development...)
  - In case you can't get these running on your computer, that's what GitHub Actions or GitLab CI/CD are for (we'll see next week!)   

- How to share the repository?
  - If you need to share a repository you own, you need to set its visibility to "public" in the settings (settings menu, scroll down). If the visibility is public, anyone can fork/clone it (but they can't necessarily write to it)
  - If you are following the exercise, and need to contribute back after you forked the repository, then you need to open a pull request *on the original repository*. You get prompted to do that if you push a new branch or new commits to a branch on *your repository*
  - Have I answered your question?


:::info
### Exercise until XX:45
https://coderefinery.github.io/git-collaborative/forking-workflow/#exercise
:::
- I am in the settings and it is public, should i invite collaborators? But i don't know theirt names
    - the instructors answered in the streaming, was it clear?
- Sorry this one was me, I did git reset by accident twice which reverted one of the changes that you did!
    - I have done "sync fork" now 
- Is there a command to see where you're about to push to from command line? 
    - `git remote -v` will show the origin and the one where it will be pushed with '(push)'
    - you can also double check by running a dry-run (nothing gets really pushed, you just see what would be the printed outcome) with `git push --dry-run` if needed (but the answer to your question is the comment above).

:::info
### Break until XX:06
:::

- do you like some topics to revist or something unclear in the next 10 min? or 
    - Demo: o
    - Forks:
    - Hooks:oo

- Would you run automated tests as part of a hook?
    - I think the instructors answered it, but in my experience you only want to run very fast tests or linters as a part of the hook. If you want to run 'slower' tests or a bigger test suit, it is useful to automate it using github actions.  
- In which language this hooks is written?
  - They can be written in any language actually. Here the examples are in bash, but they are just executed by git without looking in what is inside them. Bash is quite "easy" because you can also use other git commands inside it, probably?
  - yaml is used for github actions/gitlab ci/cd, for git hooks (the ones in .git/hooks) the above comment is valid 
- 
- .


## Feedback, day 3

:::info
### News for week 2
- This week was about basic git-based. Next week is different: different small topics directly to research!  If this is boring, come back... and tell your friends.
- Remember, this stuff is common, but there are plenty of little things to remember.  Don't feel bad asking for help (that is how every instructor learned this).
- It stays practical and there are demos (and some minor exercises, maybe), but more of "starting point and you can learn more."
:::

### Today was (multi-answer):
- too fast: o
- just right: ooooo
- too slow: o
- too easy: o
- right level: oooo
- too advanced: 
- I would recommend this course to others: oooooooo
- Exercises were good: oooooo
- I would recommend today to others: oooooo
- I wouldn't recommend today: 

### One good thing about today:
- Love the interactive exercises! Nothing teaches better than doing it yourself and getting stuck and figuring things out.+3
- Super well organized with adding us as collaborators so we could actually experience contributing. +1
    - but maybe not skipping the notifications so people know that they are reviewers?
- ...
- ...
- ...

### One thing to be improved for next time:
- Maybe start the intro to the first exercises by showing the instructions for individual learners first, and only after - for teams. It was a bit confusing in the very beginning.
- A visual for the excercises on all the forks/brances etc. and what you want to achieve. Like yesterday would have been nice.
- I prefer the possibility to speak and receive an answer than write


### Any other comments:
- I'm very interested in joining a live (if possible) shell crash course. Maybe you can conduct it again here on Twitch. 


Any other questions:
- What level is the shell tutorial on Monday? Is it for complete beginners or might I benefit from it as a kind-of beginner that already uses it regularly? :( 
  - the shell is one of those topics where you need to know very little to start (ls/cd/pwd) but there's a lot one can learn that can increase productivity. Apart from the recorded video, there is a course written in a very concise way that you can have a look at https://aaltoscicomp.github.io/linux-shell/ :100: 
    - the intro level shell course video from CodeRefinery is really good and easy to follow! (https://www.youtube.com/watch?v=xbTTDLA3txI) +1
- I always hear how productive devs are in theire favourite editor -> would you agree with that statement, knowing shortcuts etc. bumping productivity to the max - or does it not really matter
  - to my experience, working in an environment you are familiar with is a massive boost to productivity and it is massively less stressful 
  - fair point
  - that said, it doesn't mean you need to have a favourite. Just pick anything you feel like using (e.g., I tend to not care that much and switch between editors, but I have some familiarity with them).
  - I think it is important to be efficient at your tools/editor/etc.  Of course some people take it to an extreme because it's fun, but not everyone needs to go that far.  It's also probably good to experience different editors (etc) to see what you like best. +2
    - erconomics 
- Corrected the Issue #xxxx and Issue #xxxx, but it was not merged, was there some problems still in automated testin or someting else?
    - I asked people with admin rights to look at it and close it. I think everything is all right with, it just needs a reviewer. Hopefully it will be solved soon :)
    - Should be done now
    
- Many thanks!