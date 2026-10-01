+++
template = "page-with-toc.html" 
title = "Questions and notes from workshop day 3" 
+++

This document contains the shared notes activities, some direct identifiers have been removed.

## Icebreakers

**What programming language(s) are you normally working with (add an o for your answer):**

- Python: ooooooooooooooo
- R: oooooo
- Julia: ooo
- C++: ooooo
- Fortran:o 
- Perl: 
- PHP: o
- SQL: ooo
- APL: 
- Rust: 
- Go:
- Bash (shell): oooooooooo
- Typescript/javascript: o
- Java: oo
- Matlab: oo
- C: o


**What does testing your code mean for you? How do you test?**

- Write tests in Java application (Intelliji)
- pytest
- UI testing
- only manual tests +1 +1
- unit testing / feature testing
- get the "result product" I am looking for. A plot, statistical results.

## Other questions
- Is the streaming also unsharp for others? My connection is fine but the streaming is unsharp
  - you might have to select "source" in the quality
  - Thank you for the tip! It's better now, I changed the quality (which only works when I deactivate half screen/full screen I noticed) and refreshed the page.
    - mine is fine +1

## [Automated testing](https://coderefinery.github.io/testing/)

:::info
# Exercise [Automated testing on your computer](https://coderefinery.github.io/testing/locally/)

Exercise Local-1: Set up the example and test, run it and break it to see what happens
:::

Questions about the exercise: 
- in my case the test didn't pass
   - What is the error you get?
- Done in shell (content removed after issue was fixed). 1. I passed the first 3 tests. But I could not catch up with the rest of the exercises because I had to travel. I'll try to continue during lunch break. :-) 2. Update: I successfully ran the tests (3 passed, 1 failure & 2 passed). **QUESTION: what is better, conda or .venv?** So, I am trying to re-run the tests in Colab now, both with conda and .venv. [Off topic: why am I thinking of running the tests on qBraid now?] --> Existential question: is it better to learn shell coding or else, and why? PS: I am using Duck.ai as assistant now (it's a nice surprise), and interestingly it understands its own failures and is kind of good at ´self-reasoning´. I am trying to refine my prompt engineering skills and train it to understand both chain-of-thoughts (human-user limitations and model limitations/failures), but I am not very satisfied to be honest. It would be cool to kind of see who learns faster, me or the model/s. Wild, innit? I hope the lecturers won't get shocked. My approach could be useful for educational purposes for newbies or stuff. CAN SOMEONE PLEASE TELL ME IF I WAS SUPPOSED TO DO FURTHER TESTS? Sorry for disrupting. By the way, if AI models will become good enough to teach people how to learn programming, will all lecturers be soon jobless? :-) Kidding. I like to add some suspence/thrill at times. 

  - Your test did pass at first, but you are getting a host of other error messages
      - So, what to do?
          - The command you can copy and paste to the terminal is only "pytest -v exapmle.py" (without the '$'). The rest of that cell is the output you can get.
          - You might need to activate the "coderefinery" conda env, see installation instruction (https://coderefinery.github.io/installation/conda/)
              - What I think went wrong is copy-pasting the command together with the output into the terminal (only needed to copy `pytest -v example.py`)
            - i think i have miniconda <- this is fine
            Very strange, now it even doesn't find pytest((
            something very wrong in my system
```
pytest -v example.py
bash: pytest: command not found...
Failed to search for file: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Could not activate remote peer.
```
- But running this `conda activate coderefinery`, and then`pytest -v example.py` works? 
    - nothing works unfortunately, whites files not found 
    - failed to search for file: GDBus.Error:org.freedesktop.DBus.Error.NameHasNoOwner: Could not activate remote peer.

        - Please make sure you have created the file example.py (in the exercise), then check that you are in the same directory as the example.py file
            - yes , there is a file and i am in the same directory, everything is perfect but pytest doesn't work
                 - When you run `conda activate coderefinery`, do you see (coderefinery) on the next line? (does the env gets activated?) Also try running `ls example.py`, check that you can read the file and it looks okay, please. 
                 -  Oct  1 10:34 example.py file exist and it was first as you said tested, i change + into minus only_. when i give command :conda activate coderefinery, information that the file didn't found
                 -  gives "command not found"
                     - I suspect that something is wrong/missing with the conda environment. You could just try running test without the envrironment (`python3 -m pytest -v example.py`). Otherwise, check that the 'coderefinery' environment exists, deactivate, activate again maybe? Sorry, a bit hard to help with this without seeing your machine... If you have a local IT person, I would ask them for help with this :)
                     - Are you on Linux/Mac? If so, did you do the 'source'? (https://coderefinery.github.io/installation/conda/#activating-the-software-environment)

                        - Now i am installed everything and it works! It as a pity that it tooks so long and i passed exercise
                            - Ah, so nice to hear! :) Sorry it took so long. You can try the exercises later on your own as well

 ok, i will do, thanks

- I used a Colab notebook, added %%writefile example.py at the start, then next cell !pytest -v example.py and test gave a pass OK.   Colab maybe not the ideal environement for this, but can't do better now. Is the result realiable?..
    - I am not very familiar with Colab, but it looks like it should give you a Linux virtual machine (runs in Google cloud), so the result is reliable. All good :) 
        - Which would be the best/ideal environment please? I also was thinking about Colab and simply Shell. 
        
        - so this comes from my environment, not from anywhere else: I assume this is the descripton of the colab env: platform linux -- Python 3.13.15, pytest-8.4.2, pluggy-1.6.0 -- /usr/bin/python3 // cachedir: .pytest_cache rootdir: /content plugins: anyio-4.15.1, typeguard-4.6.0,  // langsmith-0.12.5
        - Yes, all the output is the specifications of the google colab cloud environment (your session)
            - yes, double checked that, useful 
    
- I  tried to define floats in Python, but did not find a way, like in C/C++, is there a way at all?
    - sorry I'm not so familiar with C, do you mean you want to declare your variable type? Or do you want to check that a variable is a certain type? Python doesn't need the initial variable definition like C or Fortran, but there are several ways you can ensure your variable is a float (for example, wrapping it with `float()`). If you are defining it as the input of a function, you could explicitely declare the type (I think it is called type annotation), but this is not needed.
    - in python variables in the code do not have a type. It feels *wrong* if you come from a Java/C environment where everything needs to be declared with a type.
    
- what is this? "Design-2 / Solution:  # What does this last test tell us? assert count_word_occurrence_in_string('AAAAA', 'AAA') == 1" > because AAAA does not include whole word (space)AAA(space)? shouldn't that be == 0?
    - It does not assume spaces ('AAA' not ' AAA '), so AAA fits inside AAAAA once. But you can design the test differently to include the spaces if you want
        - That's not how the split function works though. By default, it uses white space as a delimiter, so it should return 0.
            - Right. Sorry, I am wrong. The other way around. (so the question was there to make us think why the test will be failing?)
                - so the one in the solution "==1" gives a fail, but when I change the test to ==0 it passes
                    - I am also a bit confused now, becaue R and julia examples are different. I will highlight this to the lesson maintainers, and get back to you. Thank you for pointing this out!

## [Test Design](https://coderefinery.github.io/testing/test-design/)


:::info

## Exercise 

-> https://coderefinery.github.io/testing/test-design/#pure-and-impure-functions

Design-1 - 5 , try whichever exercise you are interested in , you can also try 7-10, but they are a little more complex :)

Design 6 will be demonstrated after the break

:::

## Demo of [Design-6](https://coderefinery.github.io/testing/test-design/#test-driven-development)

## [Automated remote testing](https://coderefinery.github.io/testing/remotely/)

Your questions here: 
- With the test examples is it possible to add some fortran examples?
    - Thank you for asking. We would like to do that, but were lacking the experts to work on it. If you have suggestions, please send an Issue / Pull Request: https://github.com/coderefinery/testing/tree/main . It actually has been a long standing open issue: https://github.com/coderefinery/testing/issues/116

- What is the github actions tab for? I haven't seen or worked with it before
    - its basically for automating tasks in GitHub.
    - GitHub can run "workflows" for you, that you define in yaml syntax. You can do *many* things:
      - create static websites and host them on github pages (e.g., with sphinx, as demonstrated yesterday in the documentation lesson)
      - as we do today, run the test suite
      - format (remove excess whitespace and make your code automatically conform to a set line length e.g. 100 chars) and lint your codebase (i.e. run static analysis on your code to find errors)
        - for the formatting, it can also re-format and make a pull request to your repository with the formatted code.  
      - you could do basically anything that one can do on command line, it is a sequence of command line commands
      - and very importantly, many "actions" are available in a marketplace that might solve a problem you have, or perform a task you would like to do 
      - GitLab CI/CD does similar things

:::info

## Exercise 

Try out [exercise CI-1- Create and use a workflow on GitHub or a pipeline on GitLab](https://coderefinery.github.io/testing/remotely/#automated-testing-remotely)

:::


Questions continued: 

- Is there original in GitHub that we fork - a link to that?
    - For python, you can fork this repo (there is R version too): https://github.com/AaltoRSE/PyTestingExample
- what is wrong: when i push it gives error failed to push some refs to origin
  - is in repository branch not main??
    - you might have to pull first: github has created a workflow file in the repository for 


## Feedback for this morning session

We will continue with modular code development after a one hour break. Please let us know how this session felt for you, by adding a `o` for your answer below.

This  automated testing session was: 

too fast:o
too slow: 
right speed:oo
too slow sometimes, too fast other times:ooo
too advanced: o
too basic: 
right level:o
I will use what I learned in this session:ooo
I would recommend this session to others:oo
I would not recommend this session to others:o

Anything else you would like to say about this session: 
- difficult entry for a first timer but i see the value and will gravitate towards this, didn't expect to understand everything but still got a good general framework on what this is about and how to modular-way/structurally begin to teach myself towards working this way..
- 10 minutes wasn't quite enough for the exercises +1
  - which ones? The first batch in the "Test Design" part of the lesson or the github actions?
- the time for the first excercises were enough, but the last one was not enough, but great cases you have here, happy to learn! 
- The first exercise (automated testing on your computer) i had enough time, the second (test design) felt rushed, and the third (automated testing remotely) no way near enough time. 
  - thanks for the feedback!

## [Modular Code Development](https://coderefinery.github.io/modular-type-along/)


:::info

## Exercise 

Look at the [starting point](https://coderefinery.github.io/modular-type-along/starting-point/) and think about what you would do to improve the code.


If you want you can clone the code: https://github.com/coderefinery/modular-type-along-exercise

:::

Your questions here:
- We have to start testing this notebook?
  - Testing a notebook is hard! But we can try something. Testing will not be (unfortunately) the main goal of the lesson, but we will keep discussing testability throughout the lesson.
      - I am brainstorming on the code cell ...
- Where are the notes from earlier today? They seem to have disappeared. +1
    - They have been archived: https://hackmd.io/@coderefinery/archivedchats 
    - Later they will be available with notes from other days at https://coderefinery.github.io/2026-09-22-workshop/questions/
- Too fast, I just cannot keep the pace on github. Would be lovely to have a documentation of how the lecturer is moving on github. I did not understand anything. What are we doing? We were supposed to clone or fork the repository. But I totally lost all the next steps. And I don't know how to connect github to Coderefinery either.+1 Now I am somewhere on crisp, my God (I am looking for the Coderefinery thing on github but I didn't manage to literally see what the lecturer did). +1
- The same to me, very quick +1
    - try to follow again, the github bit was primarily a recap of past things
    - the instructors just made a small recap, you can find the link to the repository here: https://github.com/coderefinery/weather-analysis-exercise/tree/main

- Please, explain what we are goingh to do, we check in the local directory that test are working, should we do it in the repository?
- What is the AIM?
- There is np clear aims, steps +1
    - Making the example code more modular. See https://coderefinery.github.io/modular-type-along/exercise/#coding-track
    - Indeed there are no steps in the materials, **we suggest to lean back and watch and if you want to suggest things for the instructors to implement**. +1

- The script shall be run on shell or shall we opt for the github repository option. And if the latter, how do we proceed with integrating it with Coderefinery etc? I give up. I will ask an AI assistant to help me have both options set up. I don't know even how to start. It's pointless to follow the rest at this point. After trying to clone the repository you gave us, I ended up here somehow: ![](https://)![](https://notes.coderefinery.org/uploads/6eb2fce9-533d-4e0b-9728-9995dee28e9b.png). Can you please help me understand the Coderefinery whatsoever integration on Github once we clone the repository? --> I got it, the Coderefinery option is not available (for me). Thanks. 
- Is this correct?
    - yes, it is correct. That is in case you want to follow and run things in your computer, using the terminal. Once you do that, you should have everything you need to start playing around with the repository and do modifications to improve it.
    - If you want to use Github instead, then you could do similarly like previous week (create an issue with the modification you would like to try/add, create a branch to work on it, create a PR when you think it is ready to merge :) ). The goal of this exercise is that you learn and think ways of adding modularity to your code, not so much that you create them now for the lesson (compared to first week). That is why it is perfectly fine to sit back and follow the modifications that the instructors are doing, and why they are working on them a bit fast.
    - please tell us if there is something specific of those modularity-related ideas that is confusing or you would like to understand more
    
- Follow along locally or watch. If you would like to run the exercise on your own computer, clone the example repository:[Weather analysis exercise repository](https://github.com/coderefinery/weather-analysis-exercise/tree/main). In a terminal, run:

```bash
git clone https://github.com/coderefinery/weather-analysis-exercise.git
cd weather-analysis-exercise
conda activate coderefinery
```

- As far as I understood, the best approach is to work locally (I just panicked because I did not understand that the Coderefinery option on Github was available just to the lecturer - How can we get access to this integration btw?). I actually was able to get the plots on Colab as well after all. (Colab could be useful since it combines Gemini - although I do not trust that much Gemini for coding yet).

   - sorry, it seems that we lost some of the notes and part of the answers to your question. You can still follow along, the instructors are just demonstrating things one could do to improve that repository and make it more modular (but there are many many options). You can also take a look at that repo (or one that you have for example) and try to think how could you  make it more modular :) At the end of the exercise there are suggestions that can apply to any repository: https://coderefinery.github.io/modular-type-along/exercise/#coding-track
- Please do not give up. Lean back and watch what the instructors are doing. In general the idea is that we have an example code and want to make it more modular. There are many ways to do that so the instructors are chosing steps and implementing them on stream. Right now they are working in a python file and work on introducing functions to not write duplicate code for different inputs

**To follow along with the history : https://github.com/coderefinery/weather-analysis-exercise/tree/main**

:::warning
Sorry, we lost some of the notes, please ask again if something is unclear below :heart: 
But please know that this is also the ideal time to lean back and watch. You can try by yourself outside of the workshop and we are happy to help with any issued that are coming up also then via support@coderefinery.org
:::

> Read more about [encapsulation](https://coderefinery.github.io/modular-type-along/encapsulation/)

## Feedback for Day 6 of CodeRefinery workshop

:::success
In the morning we covered automated testing and modular code development in the afternoon. 
Modulare code development lesson is the place where everything learned in the workshop comes together. If it went all a bit to fast, please know that we have the recordings available on YouTube in a bit (and you can re-watch on twitch still for 7 days). Feel free to come back to it and try yourself also outside of the workshop; contact support@coderefinery.org if you have any open questions. One possibe solution on making the code more modular can also be found here: https://coderefinery.github.io/modular-type-along/solution/

You can find all links from the concluding remarks here: https://github.com/coderefinery/workshop-outro
:::

### Today was (vote (add a `o`) for all that apply):
too fast:o
too slow:
right speed:oooo
too slow sometimes, too fast other times:o
too advanced:ooo
too basic:
right level:oo
I will use what I learned today:ooo
I would recommend today to others:oo
I would not recommend today to others:o


### One good thing about today:
- Got good pytest experience as have not used it earlier at all.
- I better understand my weaknesses and limits (from the theoretically point of view, visualization limits I guess). I'll start a free Harvard course right now (https://cs50.harvard.edu/python/). I feel stupid.  
    - I've been learning and using python for 7 years now, I still feel stupid very often. Don't get discouraged! It will definitely get easier :)
        - Thanks. The more I study, the more I feel stupid somehow. ^^ +1 :)

### One thing to improve for next time:
- Maybe some more easy or shorter excercises would help more easlity, anyways it's easy to come back later with the videos.
- ...



### Any other feedback? General questions?
- maybe better to inform beforehand that we need some background knowledge about working with git repo and bash command
    - Thank you for the suggestion. Git is part of the beginning of the workshop and we did offer a shell crashcourse just before the workshop. But we could make it more clear in preparation for the lesson, that is true. Noted. 
- Free courses and certifications for modularity?
    - Could you please elaborate? :) 
        - What could I study to better undertand "modular code development"? I kind of find it difficult to understand for some reason. I mean theoretically the concept of modularity is hard to comprehend to me. 
            - I think you can begin with two concepts: (1) pure vs impure functions and (2) testing. If you start writing test for a pure function, i.e. function that does one thing only, you may feel very easy. Then try making the function do a bit more stuffs (make it impure) and you will see how difficult it gets to write a good test. Modular code in a nutshell is all about breaking functions into manageable chunks for better readability and testability.
        - Thanks. Makes sense to me ("into manageable chunks" especially). 
          - Manageable, Readable, Reusable
- Just: Thanks a lot :D
- Excellent work all - you made me learn a lot! Thanks a million!!!
  - :) 

- I need to get an affiliation finally! Adopt me!
   :) 
- welldone everyone 
- Just a note for the lecturers: I could not attend most of the previous sessions except yesterday and today. It means, I will have to wait until all the sessions will be uploaded on YT basically. I had multiple webinars and courses overlapping, and other circumstances that made it impossible to properly follow the entire course. So, to conclude, I don't consider the speed of this lecture inappropriate nor the level of the webinar unreachable. (Do I remember correctly? All sessions will be uploaded on YT?)
    - Yes! All sessions will be uploaded on coderefinery YT channels. Most are there already!
- Great work all - in some cases I would prefer the online discussion option, as sometimes you just drop out during the 6 days and takes a lot of time to try the excercises by your own, or a help line (Zoom or Teams channel that you might be able to call would be helpful.) You would more easily get back to do the real thing. Thank you all. 
- I'll propose some further improvement/s to the code after all (via github). Please provide feedback. :-)
 


