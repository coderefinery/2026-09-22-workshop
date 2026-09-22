+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 1"
+++

This document contains the shared notes activities, some direct identifiers have been removed.

# Day 1 - 22/09/2026

## Icebreakers

Let's test the notes with some icebreakers! :icecream:

### Where are you connecting from? How is the weather there?
- Uppsala, nice and sunny
- Ioannina, Greece, cloudy
- Taipei, Sunny
- West Coast Finland
- Copenhagen, Denmark - sunny!
- Espoo, Finland
- Riga, cloudy
- Helsinki +1
- Lappeenranta, Finland -- sunny but chilly
- Reykjavík, Iceland -- light rain, 7 degree C
- Stuttgart, Sunny
- Tromsø, Norway
- Oulu, Finland - sunny and +9 deC
- Espoo, Finland, sunny +1o
- Vaasa, Finland, sunny + 1
- Tønsberg, Norway, cloudy
- Istanbul, Turkey, cloudy
- Lappeenranta, Finland - Sunny :)
- Oulu, Finland - Sunny and cool, lovely day
- Gothenburg, Sweden
- Dummerstorf, Germany - Sunny and cool (11 - 18 degrees C)
- Sørumsand, Norway - sunny and cool
- Munich, Sweet Autumn chill 
- Oslo, sunny
- Erlangen, Germany
- Helsinki, Finland (Sunny0)
- Odense, Denmark - cloudy :( 
- Karlsruhe, Germany, sunny
- Tartu, Estonia, sunny
- Stockholm, Sweden, sunny
- Oslo, Norway, sunny and cool
- Lappeenranta, Finland - perfect autumn weather
- Helsinki, Finland - sunny and happy
- La Rochelle, France- Sunny and cool
- Oslo, Norway, cloudy and sunny
- Oslo, pretty sun
- Wroclaw, Poland, cloudy
- Tromsø, Norway, cloudy
- Karlsruhe, Germany, Autumn
- France - heavenly
- Dresden, Germany - Sunny and cloudy
- Kuopio, sunny
- Bakary, Sunny

### How are you attending this workshop?
Poll: Add an 'o' to the answer that applies to you
o
- By myself: ooooooooooooooooooooo
- With colleagues/research groups: oooo
- In a classroom: oo
- At home with my dog: o
- At home, in front of the window 0o
- add more...
- From the office: o
- Online from home o


### What's a recent project you want to tell us about? (work or otherwise)

- Tangled up in a version conflict, Github vs local folder, also trying to update a branch into a main version ;D 
- Preparing a lecture on literature review with (and without) AI
- Automating lab workflows
- ..
- ..
- ..
- I have been working on a pipeline to process fusion gene calls which I could really use git to help with!
- SearchSEO- Method-Level Code Provenance Across the Open-Source Supply Chain

## What's a recent cool thing you have read or learned?

- Some podcast about AI hype and bubble, I need to find the link
- I learnt how to make fire in the summer and practiced that skill in parks
- Dune Book 2, how a "hero" can become the victim of his own success
- The computer display can break easily, and costs for a new ones are cheap nowdays. XD
- I really enjoy the Nakki croissants from lidl and have been trying to make them at home, mixed currently but we carry on
    - I have to try that
- I've been experimenting with "AI" coding to learn about it with some toy projects.
- I have been reading the books of Edouard Louis such as "The End of Eddy", "History of Violence", etc.
- I can finally get the functions I need for different processes, and now learning to keep track of tHAT process 
- I am reading Memories of Adrian by Marguerite Yourcenar
- Efficient and effective using of Claude 

## Any other questions or comments, write here below
- Great sound quality and video!
- So far, awesome prep for the course!
- Didn't get the new display yet, so following this on a 14" screen is a challenge for today.
    - We try to make it workable with the portrait screenshare!  Always write here in the notes if we need to make the font larger.
- "If you have registered to attend breakout rooms" - where did this happen? how? 
  - Some countries or locations have local classrooms (in-person on online) that do the exercises together.  I think we to people rooms that are relevant to them.
  - I am not sure  if this was an option for me. How do I check this? The online?
      - The local class rooms are listed here. https://coderefinery.github.io/2026-09-22-workshop/#local-exercise-groups
- We don't hear the audio of Diana well (it's also very hard to hear her) --I have the same experience


## Introduction
https://github.com/coderefinery/workshop-intro/blob/master/livestream.md

You can (always) continue asking any more questions at the bottom:

- There is no pop up on the gear button to adjust the quality :/
    - For me it didn't come up when in fullscreen but did when I stopped fullscreen. 
    - will check once the quality drops again
    - it disappears for me if I "pop out" the player and it is not any more inside a browser tab. I need to be able to see the whole twitch interface (the coderefinery banner, the number of listeners and so on) to be able to interact with that button and change the quality
        - Yes, it is the same for me. First change the quality in the "full" interface of twitch and then pop-out or swith to full screen
        - reload of the webpage did the trick as well :)

- . What is the difference between github.com and a university-based github platform (e.g., github.uio.no)? I have a profile on each but they are completely separate. I am not sure which one I should be using regularly as my main profile.
  - If your university has github enterprise then most of the experience should be the same as on github.com. I am not sure if you can fork repositories from github.com... can you?
  - If you change your institution at some point you might lose access to the github server of your current institution, so you might have to migrate your projects to a "public forge" (which is not hard, but can be time consuming) 
  - From a University point of view using the uni forge is preferable, one idea can always be to have two forks (one on the uni servers, one on github) the uni servers also have the advantage that they are not directly controlled by companies - who tend to train models on whatever is there). E.g. for research, you could use the internal before publication and then push to the public upon publication. 
    - Adding to this: it is possible to make so that one repository is automatically update when the other is (using "mirroring"). This automation is a little advanced though (although, next week we will see the basic of the underlying technology, "github actions") 
- .
- .

## git-intro day 1
o

- Can I delete a commit from a list? (I know thtats not the point but if there s something critical that should not go online? by accident)
  - This is an example of "rewriting history", and it is possible. The last commit can be changed more easily (git commit --amend), the previous commits require also the subsequent commits to be changed, so it's a bit more involved... (git history fixup in new versions of git , or git rebase more in general, but it's a little complicated. If you really need to do that, you'll have to look up these commands and learn how they work. Hopefully it happens rarely)
  - And be aware, that even if you rewrite history, the commit might still be around on github or another forge and accessible via the object id, especially, if here has been a branch that still contains it etc. 
  - keep in mind if it was already pushed online, need to rewrite the history and then force push
    - this risk is there if you have accidentally pushed already the "critical" commit
- .Is it possible to make the "sunglasses" branch the new "main" and ditch the "main" altogether?
  - yes you can make the sunglasses the new defult branch, and then delete the old main, you can then rename the sunglasses to main to keep it as a usual name branch
      - But you don't need to have a "main" branch, it's "just" convention to have it.
- .If you are working on different scripts within the same project, does a branch only apply to one of these scripts or can a branch apply to multiple scripts
  - no, it applies to the whole repository (as a commit does). A commit is a snapshot of the whole repository, and a branch is "just" a pointer to a commit.
  - so your branch can contain changes to few scripts and files at the same time 
- I think I tried to delete something in a branch + did some other useful changes -> then merge to main -> so the main obviously has the deleted part still "in", although I wanted it gone. Missing something in this workflow?
  - maybe your deletion was not commited and you merged, a safe workflow is you run `git status` after deleting what you want, to get sure Git shows the deletion, then commit and merge. 
      - To clarify, if you just delete a file, git doesn't register this automatically. To have git notice you either have to use `git rm <filename>` or explicitly add the deleted file `git add <path/to/deleted/file>` before commiting otherwise it will not be added to a commit. 
      - Use `git status` as your only source of light in a world of darkness, and you will see
  - so the basic idea is that after committing the deletion in a branch, it SHOULD disappear from main as well, after merge?
    - yes, that change would be applied to `main` as well when merging (merging is not only for adding content, but also for deleting content)
- Is there a difference between forking and working on a branch? If so what is the diff?
    - Fork is a complete copy of the current state of the repository to your own workspace. You have control over the copy, not the original repository owner. Within a forge, a fork is also often linked in to some form of fork network, where e.g. if one fork gets deleted references might be updatedpointing to another fork and (at least it used to be that way), data in a fork network can be accessed from all forks, even if one fork is set to private (this might have changed). In contrast a branch is "just" an alternative version wthin the same repository. One more thing to note with forks is that there are two ways to create a fork. On the forge platform (github/gitab/bitbucket etc) or by pushing a repository to a different remote. The latter will commonly NOT add the fork to any existing fork network and "just" creates a copy at a different place.
- Can I fork my own repo for myself?  Or just create a fresh copy somehow, if I don't want all the history? 
    - GitHub does not let you copy a fork of your repository under the same accont. But you can fork it under a different accont/organization that you have access to.
    - Also we need theOne way of bypassing this is to clone locally and then push to a different repository. But that is not strictly a fork.
    - Also: A Fork (by definition) contains all the history. IF you want a history-free copy you essentially need to copy the contents of the folder to a new local git repository add and commit it in there and push that to a forge. 
- Is it possible to find exact matches in the seach bar? for example, now if I want to find 'oil', it shows 'boil' too
- When i search for a keyword in my fork of the repo, it says I cannot search because my fork is 'currently being indexed'. What does that mean? I can search in the upstream repo.
  - its because Github stil preparing your fork so you can search init afterwards, you need to wait until it finishes indexing the fork. but the upstream repo is already prepared, so you can search in it.
- 

### What is version control useful for? When would you have needed an old version of your code?

- I'm debugging and try many things to make the code work, most of the attempts don't bring me anywhere and when I finally find the fix I want to get rid of all the failed attempts
- I am working with a team for creating workflows, so it helps us in keeping a control of these projects.
- I used it for comparing the newest version of  my phd thesis against and older version and then create a version with highlighted changes.
  - Are you using latexdiff?
  - Yes, I think I used latexdiff. I tagged the older version I wanted to compare against. :+1: 
    - More people should know about latexdiff! At least among those who use latex heavily.
- Keeping control of version control seems a skill too... when to create a new branch, when to just use whatever currently in
    - Definitely! It takes some practice and experience to figure out when use them. It also depends a lot on the project you are working on, for example is it a collaborative one or is it only you? We will talk more about good practices regarding branches and other details later on :) 
-  


::: info
### Exercise untill XX:05

https://coderefinery.github.io/git-intro/browsing/#exercise


I amo
- done: oooooo0ooöoo0oooo00
- not done: oo
- not trying: oo

:::

- The commit messages of the most recent commits are not very descriptive/helpful compared to earlier ones.
  - Yes, that's a good point to think about!  What's the balance?  What's worth it.  We'll try to discuss.
    - See also: https://coderefinery.github.io/git-intro/level/#writing-useful-commit-messages with additional references in that section.
- I cannot find an "issues" tab only one for pull requests
    - The "Issues" tab should be just to the right of "Code"
        - For me that is just "Pull Requests" then "Agents Actions Projects Wiki Security and Quality Insights and Settings"

            - Make sure that issues are not disabled for the repository. Go to Settings → General → Features → check “Issues”
                - Yes this was it, many thanks!
    - In your own fork, issues are disabled by default (the idea is that most discussion by default happen in the upstream repo/teh one you forked from, but you can enable it).  If you look at the original one I think you'll see them.
- in Github, there is my annoying mouse cursor hand on top of the little info boxes that will open when hovering over - if the info box happens to open underneath (like when looking at blames)
- When I search for 'salt', I get this: This repository's code is being indexed right now. Try again in a few minutes.
  repo:username/recipe-book salt
  Why?
    - This is normal for a newly created fork on GitHub. GitHub indexes all the files, so it takes a bit before "search" is functional. Just try again in a few minutes.


::: info
### Break untill XX:15
- Do you want a demo of the exercise? (See also [walkthough under the exercise](https://coderefinery.github.io/git-intro/browsing/#solution-and-walk-through))
  - yes: oo
  - no: ooooooo
:::

Exercise discussion:
- AI suggestions come up when commiting changes - recommended to use / not? of course if helpful, why not, but thinking about the whole "AI issues" perspective 
  - A very good qusetion.  In one sense I think "well, that's nothing new that wasn't in the changes anyway.  Let someone use a better AI in a year to describe it if they need it".  But a quick summary now may be useful, anyway.  I generally think the biggest problem with AI is making to much text to read (and like below, miss the point of *why*).  I would avoid using in general.
  - I find that typically AI suggestions tend to miss the point, because AI typically does not know *Why* we made a change, and can only read *What* we changed. 
  - Yes, I find them too verbose, usually, or too particular, sometimes spot on. Can't decide if I want them popping up or not (would like to "prompt" it to use my preferred style ;D)
- Is there always a license file? What if there isn't one?
  - The license needs to be actively added 
    - Without a license granting additional rights, you generally shouldn't assume you may redistribute, modify, or incorporate the code into another project.
    - in other words: if *you* don't add a license, nobody can feel free to modify the code and reuse it
- Just a suggestion: It would be helpful to have a live demo for each exercise, as participants in this course have different levels of experience. 
    - Noted, we will let the instructors know :)
    - Thanks for the feedback, it is tricky to keep the course as good as possible for everybody so getting your suggestions help us a lot. Keep it coming!
        - One more thought: Live demos would also make the YouTube recordings more useful for people who want to follow along and practice the exercises afterwards.

- How can one rename a branch they have created?
  - if you are on that branch, you can do `git branch -m "newname"` then push the renamed branch `git push -u origin "newname"`. you can also delete the old remote name afterwards.
  - you can also do it on GitHub by clicking on the branch dropdown menu, selecting "View all branches" and then choosing "Rename branch" for the branch you want to change (you can find it by clicking the ... symbol)
- My tags kept failing because of invalid tag name. What does it expect? I tried using words separated with_ and i tried like vx.x.x - I was confusing tag name and title as the same thing,which they are not. Fixed now.
    - the tag is a pull-down menu on the top-left 
  - nice :) 
- It might (?)  be best if in the demo you did the excercise in the Exercise. And use same names.
    - +1
- .Your video screens are on top of the browswer address bar - but apparently the /compare goes after the repo name
    - yes, sorry about that. You can see it now
- Compare goes to the main fork cr-workshop?
    - solution for comparing own repo main and branch: wrtie address bar github. com / YOURNAME / YOUR REPO NAME /compare/main...NEW BRANCH NAME
- Merging assumes two changes are compatible. But that's not always the case (e.g., someone writes 'add 1 spoon', and someone else writes 'add 2 spoons'). In coding, lines of code can interfere in more complex ways.
    - Correct.  At some point we will talk about these, called "conflicts"
- Your video screens are on top of the browswer address bar!
    - yes, sorry about that. They did the same as in the solution steps: https://github.com/USER/recipe-book/compare/VERSION1..VERSION2
- couldn't get the compare thing working at all
    -   solution for comparing own repo main and branch: wrtie address bar github.com/ YOURNAME /YOUR REPO NAME /compare /main...NEW BRANCH NAME
- What does the "-u origin" option mean for pushing commits?
    - `origin` is a normal argument and says where to push to.  `-u` means "record this as the default upstream" - basically the default pushlocation.
- what is the difference between 'tag' and 'release'?
  - 'tag's are a "fundamental" feature of Git - you can create them even on your machine and push them to github if needed. Github has some additional ceremony around tags and releases 
  - 'release' is essentiall like a tag (unchainging pointer to one point in history) that appears on the sidebar as a "release" and you can attach more downloadable files to it (like if you need to compile or build the application).
- could you repeat what you just said about adding a source code (?) please
    - Was this about the full download of source code?  If so, you can download a .zip or .tar.gz archive of all the code, if needed.
- How do you manage release/tags with version control (doi). What's your process?
  - For DOI, I have set up [Zenodo](zenodo.org) to create one automatically. Then I create a release like we just did on stream.
      - do you have this workflow written up / flowchart-y way described anyhwere?
          - no, sorry. It's mostly automatic after the setup. / ok, i looked it up,  seemed pretty logical on paper at least, thank you for the tip

- **can you repeat the comparison please?** +1
    - We will show it again after the lunch break :)
 


::: info
### Exercie untill XX:50

https://coderefinery.github.io/git-intro/commits/#exercise

I am
- done: oooooooooooooo/[overtime]o
- not done: 
- not trying: ooo

::: 

- I am not able to find the changes I have made going to Insights -> Network I see my name but not more
    - The network graph takes a while to update. Check after luch?


## Lunch
:::info
## Lunch until xx:00
- Then we will show how these changes can be merged together and actually contributed to the joint recipee book.
:::
What did you have for lunch?:
- Quinoa salat and cardemom bun
- Potatoes and Quinoa patties
- Bacalao
- Spaghetti aglio e olio
- Turkey gouda pickle bagel and a protein smoothie
- Fries
- Chicken sandwich
- grapes and saftevand
- crispy chicken wrap
- vegetarian-lasagna.md
- code
- Rice with eggs and cheese
- lab work :/


## Comparison continued
(we'll re-demonstrate the last part before the break before going on to the afternoon part)


- anyone else getting an echo voice from the instructors?
  - Do you have two Twitch windows open by any chance?  (though there are many times we do accidentally have audio loops, too!)
  - yes, accidentally on the background, thanks! a hundred windows open here 
- Is this how you would usually compare things?  Is this harder somehow because we are comparing from a upstream to our copy?
  - On GitLab it is a little easier, or on the command line it could be a little more convenient.
    Also, your favourite editor might have good support for git and allow these kind of comparisons
    Also, the comparisons are a bit more convenient to access when doing code reviews (we will see this later this week)

- having used the command line a bit, i understand the push towards it, yet I am a very visual thinker, so i haven't solved yet how the command line users mentally process the whole thing - i rly think the command line is not a way for all to keep track of the big picture
  - Apart from, possibly, familiarity - which plays a big role - the command line interface is typically preferred by some 
    mainly because everything you do on the command line is done via text, which can be seen as code
    ... and code is the best way to achieve reproducibility.
    Going from CLI to script is much easier than going from a GUI to script.
  - I heavly use the command line but also there are some times the right graphical application is just what you need.  For sure it's harder to get the mental model with command line things, but if you know what to type (and it works) it can be faster.
  - One difficulty with visual tools (to me) is often, that when the configuration options get a bit more complicated, I start to have to click, click, click through several levels of menus, that might be quite large due to the large variety. Command line, especially with git offers a load of autocomplete functionalities, like git add s -> tab -> f -> tab -> f -> tab-> 1 gives me git add src/folder/file1 while in a UI I would need to search for the respective files and folders and then likely right click -> git -> add, which (for me) takes a lot longer. However, thecommit history is something I do regularily look at in UIs, since there having a "nicer" visualisation is useful. I think it's mainly a "do I want to give commands -> Command line" do I want to inspect something complex -> some UI tool.

- will videos from tomorrow's session be posted? 
    - They are all on Twitch for 7 days, we try to upload to YouTube for archival (how much processing we can manage to do is another question - some years we have done a lot of processing, perhaps not this year)
-
-




## Merging changes and contributing to the project
https://coderefinery.github.io/git-intro/merging/

::: info
### Exercise and break until xx:10
https://coderefinery.github.io/git-intro/merging/#exercise
(don't forget to take your break)
:::

- After selecting a branch, there is a yellow box with "BRANCH NAME had recent pushes  [green button] compare & pull request"  // Below that: "This branch is ..commits ahead of... [grey button] Contribute" -> click (opens) -> [green button] open pull request // Q: The two green buttons lead to the same function? 
  - compare and pull request (the first button) is, to my knowledge, only a shortcut equivalent to the second one
- .Re: Merge pull request. I see 3 options: Create a merge commit, Squash and merge, and Rebase and merge. What are the differences?
  - create a merge commit keeps all your previous commits anf add one extra, when you squash you will combine all the commits in your branch into 1 commit ont he main branch. Rebase keep your changes on top of main seprately.
- Is there a way to un-merge a commit?
  - yes, you can try reverting the merge by opening the merged pull request and clik "Revert", Github then creates a new pull request which undo the merge.
- what if I don't delete the branch but  I continue on it and, after that merge which just happened, offer yet again new changes to the main? 
    - Yes. If it has been merged, you need to do a new pull request. If not yet merged, the pull request will show your newer commits.
- is there a history of branches somewhere? 
  - yes, in the repository you can chek the inslights --> activity. also check this:(https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository/using-the-activity-view-to-see-changes-to-a-repository?) 
  - in the above link 1st image, what is "a closed branch" (red one)? ; this view doesn't list "deleted branches" (well it does, workaround: All branches > Branch deletions, but i don't see that option in Insights, instead I see it on the Code-page, right hand side, first heading About -> Activity)
- is it possible to unmerge after deleting the branch?
    - On GitHub, there is a "revert" button aftyer the merge. It is also possible to revert merges locally.
        - can you show where to find this 'revert' button on Github?
            - On the pull request page:
              `@githubusername merged commit <hash> into <organization>:main`
    at the right of it is it "Revert"
        But you need to have write permissions on the main branch, otherwise you may not see the "Revert button"
        - deleting the branch does not remove the merge, so you still need to revert the merged pull request.
      -  
- If I have already made many changes in my own main branch, but I want to send only one new recipe to the original CodeRefinery main branch using a pull request, is that possible? Or do I need fork again your clean main branch and then just make new recipe and do the pull request?
  - you might need to create another branch that contains only the changes you want, and then you can make a pull request from that branch (I am assuming you have made many commits to your own main branch).
  - You can also just add another commit on the top of your main branch (or on another branch, that starts at your main) where you "clean up" all the things you want removed, and then create a pull request from that commit (more precisely, from the branch that points at that "clear" commit)
  - This depends on whether you have: 
    1. Commited the changes already
    2. How big your commits are.
    If you have commited everything already, you will not be able to directly use the branch that contains everything. If you have each recipe in a individual commit, you can e.g. create a new branch based on the upstream main (something like : `git checkout upstrea main` `git checkout -b new_branch` and then cherry pick only the one commit: `git cherry-pick <commitID>` then push that branch and create a merge request from that branch. If you have multiple recipies added in one commit: see the solutions above)
- I have tried to merge from my branch to the non recorded repo and it says there are conflicts that must be resolved? I added a new file but also edited the fruit salad recipe earlier, so I'm assuming it is the fruit salad that is the problem?
  - conflict means both your branch and the other branch changed same file. so Git can not undrestand which version to keep. you can see which files exactly has the cofnlict under the "resolve conflicts".
  - This means that you have to first *merge the remote work* into *your* line of work, fix all the conflicts, and only then you can make a potentially successful pull request (If I understand correctly your situation)
- It sas that the changes can be cleanly merged - should i try to resolve the conflicts now and see what happens?
  - If the changes *can* be clearly merged it should mean that there are no conflicts (?)
  The warning states: This branch has conflicts that must be resolved then changes can be cleanly merged written underneath.
  - Ah, ok: yes, the the changes can be clearly merged only once the conflicts are solved. The way I proceed in this case if first to merge "the other way", meaning the main branch of the non recorded repo into your branch. Then you can fix the conflicts. And only then your PR can be merged
    - OK thank you :)

## Resolving a conflict (demonstration)   
(add your questions here)

- .wait what: which proposition was "current change" and which one was "incoming" , ah "current change" = "currently in main"? 
  - "current change" means the version in the branch you are currently on, but "incoming change" is the version from the branch you ar emerging in.
  - When resolving a merge conflict, Git/GitHub shows two competing versions:
    + Current change — the version from the branch you are currently on (the branch receiving the merge).
    + Incoming change — the version coming from the branch being merged in.
    + Accept both changes — keep both versions, usually one after the other.
    + Manual resolution — edit the conflicting section yourself, combining or changing the text however you want.
    I personally prefer "accept both changes" or "manual resolution" as it can be confusing which branch is merged into which.

- Note (from past experience): sometimes brand new repositories get penalised with resources. I think they do it to limit freeriders.
- .does the "current thing in main" always have the upper hand in the sense that it will be offered as the default in the merge?
  - if there is a conflict (i.e., git can't tell how to merge), then there is no "upper hand", unless the "merge policy" (there might be a more proper name for this) is specified (e.g., when pulling with "--theirs" or "--ours") 
    - ok, so no preference eg if either one is older? just that there is a difference matters Ah, funny me, of course there is a time difference ;D. 
      - (this might be irrelevant, if so,please ignore) so, if a change was made on top of some other changes on top of some other changes (...) on top of main, then it takes "precedence" when merging into main. But that's only because the chain of "diffs" (patches) corresponding to each commit can be applied  one after the other without problems.
- .
- .






## Feedback for Day 1 of CodeRefinery
:::success
Today, we covered everything in the schedule: the basics of git version control and various aspects of the GitHub user interface.
Day 2 moves to your local computer and gets to the way we really work.
For day 2, If you plan to do the exercises please make sure you have:
- a working git installation in your computer (e.g. with VS Code or with the shell terminal, see instructions at https://coderefinery.github.io/installation/)
- GitHub account
- VSCode (recommended, if you don't know what to do) OR git from the command line

If you had/have issues with the installation, we will provide a 1h support zoom session tomorrow morning 9:00 CEST (Oslo/Rome). More info in via email. Let us know if this is useful with some emojis.

Twitch will store this video for 7 days, and hopefully it will be on YouTube by the time that expires.

Day 3 is when we will collaborate together and we will send you detailed instructions on how to do that via email later today.
:::

### Today was (vote for all that apply):
- too fast:oo
- too slow:
- right speed: oooooooooo
- mostly right speed, occasionally too slow: ooooo
- too slow sometimes, too fast other times: o
- too advanced:o
- too basic:o
- right level: ooooooooo
- I will use what I learned today: ooooooooooooooooo
- I would recommend today to others: ooooooooooooooo
- I would not recommend today to others:



### One good thing about today:
- Learned a lot new on github!
- Federico made things easier to understand by explaining the backgrounds and what was happening. +6
- It was useful to interact with a repository basically in sandbox mode without the fear of doing something wrong! +2
- Having the demonstration was good, it made the concepts clearer and we could follow how you did it.

### One thing to improve for next time:
- It would be great if Diana speaks a bit louder and clearer. Sometimes it was hard to hear her. I had to turn my speaker to the maximum level to hear her +1
- agree - I think her microphone is on her headphones which is not good. We had problems hearing her in the room set up at UiO and had to leave because her sound was impossible to hear
    - Sorry about this, if this happens again you can mention it anywhere on the notes as soon as it happens and we will fix it right away. This is important because we could hear her fine from the streaming room, so we didn't realize.
- The levels of the mics differ from each other a bit, but nothing serious, at least I had volume enough.+1 
    - I second that. The volume varied considerably between speakers; some were quite loud, while others were very quiet - even when using an external speaker.
    - with a small external bluetooth speaker no problem with mic sounds, so maybe add that suggestion to instructions?  
- Would it be possible to use platforms like Zoom? Twitch is blocked by our IT and I had to join on my mobile phone. It was a bit challenging to follow with the small text
    - Yes last time one person had the same issue. We need to try YouTube as streaming platform. Out of curiosity, in which country are you based? 
- If a question can be answered by a demonstration, please do it. We'd love to see how it's actually done rather than reading the answer here. In some cases, it's also faster to show than to type here.

### Any other feedback? General questions?
- ...I would like help with set up tomorrow. Thank you. What time should I join the zoom? Thanks!oo
    - i was away fro 2 minutes - is this setuphelp happening in Zoom? 
        - Yes I will send an email and open the zoom about 1h before the streaming (10am Helsinki)
- Thank you! This was the first time I used seriously Github through the web interface. I have used only command line for the git before. Very clearly presented. 
- Thanks a lot - very helpful!
- Could you also please Merge all Pull reguests to see al the final changes and so we can try out the Sync fork feature and see our changes - thanks! 
    - +1 
- Could you also please show how to delete old repositories in a Clean way, also the local copies to free space. The Deletion of the branches could be helpfull as well to see once again.
- Thanks! Have a nice day ahead!!
