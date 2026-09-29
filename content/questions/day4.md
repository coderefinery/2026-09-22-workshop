+++
template = "page-with-toc.html" 
title = "Questions and notes from workshop day 4" 
+++

This document contains the shared notes activities, some direct identifiers have been removed.

## Sep 29 - Day 4 morning - [Reproducible research](https://coderefinery.github.io/reproducible-research)

### Icebreaker 

1. Have you heard the sentence "hmm... works on my computer"? What does this mean in practice? How do you solve this problem?
   - That very often, they are using a different OS or just OS version and some library that was deprecated is still present on the machine and I can't get it to work... 
   - Different environments... Solution; use uv (for Python) and maybe Docker containers :)
   - This is happening to me a lot at work. I'm trying to document everything so that other new people can figure out why things don't work on there machine. But its difficult to figure out whether its the os/env/data version etc...
   - Many times, not by me. XD
   - Many times, and then I have to go and try to make it work for both of us / all of us (often a Windows-Linux incompatible, different versions of R/python)


2. What are your experiences re-running or adjusting a script or a figure you created few months ago?
   - Yes and the pain was real (thank you reviewer 2)
       - Well, reviewer 2 had a point :) 
   - That unless i documented my setup really well, things don't work as expected or I don't remember how to use my scripts
   - Not always so easy.
   - If it is a couple of months go, it usually works, but if it was a year ago - very little chance of it working properly again :(
   - hashtags need to be consice, not novels, yet have enough infomation, the balance


3. Have you continued working from a previous persons script/code/plot/notebook (or your own, a year after you wrote it)? What were the biggest challenges?
   - no documentation of Python dependencies at all...
   - updating libraries etc due to security issues -> something in code doesn't work/needs fixing
   - Going through and 'modularizing' one long script... very very long one
   - Missing comments or details.
   - Finding all the input and output files created by the script (often throwing an error, as paths are set up for my colleague's machine)
   - Code missing parts or scripts, so it needed more work to be able to restore it



### [Introduction - How it all connects](https://coderefinery.github.io/reproducible-research/intro/)

Your questions here: 
 - Do we need to have docker installed for today? My docker installation broke a few weeks ago.
    - This week is more like "demos" but you can replicate what you see if you want to try things out and learn by doing.
    - Short answer: No. Longer: we will demo some things with docker, but you don't need to replicate. Docker also requires system administrative rights, so we can't require it anyways.

## [Motivation](https://coderefinery.github.io/reproducible-research/motivation/)

## [Organizing your projects](https://coderefinery.github.io/reproducible-research/organizing-projects/)

Your questions/comments here: 
- where do you place raw data / somewhat cleaned data, if you use it in multiple simultaenous projects? outside the top folder "project name /" or still inside (copy)?
    - Answer by instructor: Separate place for data documented in README, ideally data is in public place, if not possible on your own system with the README pointing to it, for others saying to contact the authors. Download and installation instructions including where to change the path so that your program can find the data
    - If data is "small", I store a copy under the same project folder (small for me is less than 1 GB), but that is just about being practical and have projects that are self contained. Otherwise it is best to have only one source as answer above.

- could you please give a brief intro to templates? No idea, what these contain
     - Shown now on stream (last link from the list)
     - They can for example give you an empty folder structure for your project which you can then populate with your data
     
- I have interrupts on the stream, is it only due to my network?
     - stream ok here +2
     - Thank you for highlighting, it seems to be your network.

- as for the src/ folder - what if you have python juplab notebooks, R, other software, all separate workflows etc - still all here in src, or subfolders under src? 
    - In my experience, there is not a single way to do it. I prefer different subfolders for different languages, but I was part of projects with scripts like step1.py, step2.R, step3.ipynb  all in the same folder.
        - yes, really interested in hearing what kinds of structures have worked for ppl, as no single solution - eg subs by steps / subs per language etc

- A lot of the repos I work on have these files pyproject.toml and mkdocs.yaml. What are these for?
    - pyproject.toml files serve as the configuration file (for python projects), they manage metadata, dependencies and some other settings. So when someone  runs the install of the code, the toml file is read, and it installs dependencies (checks that all the dependencies are installed) and packages the code; so you don't need to manually install all the packages or libraries one by one, basically.
    - mkdocs.yaml is the configuration for mkdocs, which is a tool for producing documentation (typically HTML). More about this tomorrow (not specifically mkdocs, but similar tools)


#### [Excursion: Reproducible publications](https://coderefinery.github.io/reproducible-research/organizing-projects/#excursion-reproducible-publications) 

- How do you collaborate on writing academic papers?
  - Depends on whether I am the main author. If so, I try to use Overleaf, and share scripts via github. But now I am a collaborator on another paper and I have to use MS Word in the Box (which is really annoying), but it is really hard to convince 'more experienced' colleagues to switch to another tool. I still work with the scripts via github, cause I am the main analyses person for this paper.  
  - Overleaf or google docs, with comments for discussing changes, and meetings to go over comments otgether in person.
  - I try to use latex and git, with some people it works, with others... they just want to use overleaf (but then run into problems with the maximum number of projetcs they have, version control is not that convenient as with simple git - at least for me, and so on)
    - latex+git has the advantages that you can use latexdiff :+1:
  - generally using github, but after some time being away from coding, I encountered R markdown :D which was new for me. Would be great to have a brief lecture on that. 
      - It was mentioned by the instructors, there is a tool called Quarto now. Which could be more usefull if you are using more than just R (Quarto supports other languages as well). If you are new to RMarkdown anyway, I would just learn to use Quarto instead.(thanks!)
  - Overleaf, or whatever those that do not want to use overleaf want to use. 



- How do you handle collaborative issues e.g. conflicting changes?
  - Main authour decides O.o
  - I talk to the other person and sort it out "off line". Sometimes we can't reach and agreement on the most important viewpoint to add, so we add both 
  - Meetings
  - We can never convince the professors using such kinds of tools so the most practical way is to tag files and send by email
  - 
  - (share your experience)


Questions continued: 

- Could you, please explain more about LICENSE
  - The session this afternoon ("social coding") will have a lot about that (and it has just been reviewed thoroughly) 

- And what about security? Is it safety to put your stuff online? +1 Nowadays many enterprises try to escape using even AiI onlne but use such systems inside their servers (ollama, for example)
  - if you eventually plan to publish something, unless you are afraid that you research could be stolen (which it seems could have happened, even in recent history) doing things in public shouldn't be a problem 
  - if you are working with sensitive/personal data you need to take extra precautions, and if you are using AI you need to be in control of the infrastructure
    - also, might not want to have less-than-good-ideas-on-afterthought (*adjective word edited) (esp on sensitive stuff out there, and let's be honest, everyone has those moments where you go oh no [not thinking about innocent blunders here, you get the drift]
    - on the other hand, if you have your research online early enough, it can give you more visibility (so maybe not at the very beginning of the project, but when it is half-way done?)
        - yes this is good when you feel ready for it, and lots of science is, i suppose, missing such early discussion (pros and cons exist, fo course, out of scope of this day's content) 
    - when you say 'half-baked ideas' and 'oh no' moments, are you referring to something specific in what i posted?
        - i do not know what you refer to, this was just an (half-baked) idea


## [Recording computational steps](https://coderefinery.github.io/reproducible-research/workflow-management/)

Questions continued: 

- A comment: "imperative style" tends to be easier to debug (it's easier to answer the question: how is something done *exactly* in this analysis? What are the steps from beginning to end?)
    - Absolutely. Imperative is (as long as its clean code) simply readable, while declarative needs more thought/understanding of concepts.  
    - Also, declarative is "lazy", meaning that steps are run only if they are needed to produce an output (also intermediate) 

## [Workflow solution using Snakemake]()

- Does it matter what you name the variables in the curly brackets? it seems to treat file and book the same or is there a difference?
    - No, but stay consistent
- What happens when a book is deleted? Output also will be deleted? :+1:
    - Files that depend on it will stay. 
- Is this snakemake installed on each linux/Unix machine?
    - Not by default, but you can install it, for example by following our installation instructions: https://coderefinery.github.io/installation/conda/ or find a suitable way from Snakemake documentation for your system/ways of working: https://snakemake.readthedocs.io/en/stable/getting_started/installation.html


## [Recording dependencies](https://coderefinery.github.io/reproducible-research/dependencies/)

Questions continued: 
- What are the differences between, for example, conda and uv? Which one is more popular at the moment?
    - Not sure which one is more popular, but uv is a Python-focused package installer and project manager, while conda is a general-purpose (cross-language) package and env manager


## [Question to the audience](https://coderefinery.github.io/reproducible-research/dependencies/#exercise-demo)
###  Which version is most reproducible:

5 students (A, B, C, D, E) wrote a code that depends on a couple of libraries. They uploaded their projects to GitHub. We now travel 3 years into the future and find their GitHub repositories and try to re-run their code before adapting it.

Add a `+` for your vote:

A: 
B:
C:  
D: +++++++++
E: ++++

Questions continued: 
- How do i handle being asked to code review when the code does not run in released version but in a developer env? How do I ensure im testing it in the right env?
    - Answered in stream: the developer should provide you with the instructions to run the code, including the environment. If it doesn't run, then you say it does not run. 


## [Recording environments](https://coderefinery.github.io/reproducible-research/environments/)

Questions continued here:
- Does docker assume anything about the hardware of the machines they are being run on? For example:  GPU architecture.
  - There might be some software in the image that requires some particular hardware to work. This is common. For containers to be "portable", the software in them needs to be built with portability in mind, but the "building of software" part is kind of independent from "building the image" (although in the image definition file, the build steps of the software can be defined). So the answer is: it depends on how the software in the container was built
      - Ok, so it means that docker image should be shipped with hardwarde and software specification to ensure reproducibility.
        - Ideally, software should be all contained in the container (not in the *image*)
        - Also, the software in the container should be built in a portable way (most - at least many - toolchains offer ways to build software that works on multiple hardware versions)
- What is the difference between an image and a container?
  - Image is something static, a file, a snapshot of a running container (at the beginning , or at at some point later, done for example with "docker commit"). The container instead has running processes
  - For some container tools (e.g. Apptainer) where the containers are immutable, it's kind of fine to confuse the two (there's a one-to-one correspondence)
- And if we put some software into container, and this software is liscenced how to get this liscence inside the container?
    - You can add the license at runtime instead of hardcoding it in the container. You will need to provide the valid key or license file when starting the container, and the application will unlock
- What are the trusted sources the instructors are talking about? How do we know which sites are trusted?
  - "official" images uploaded by "official" accounts that have many images, used in many projects, and that are referenced in other places are typically a good bet

- Can i inspect what folders and permissions a Docker project requests before running? how? good link maybe to this exists?
  - When doing "docker run" you typically choose what to mount (which directories of the host system are visible and writable inside the container) with the `-v` option. Typically this should be documented with the image, and depends on the software installed in the image (it could decide to open files at a given path)
    - does this course demo this? if not, a good link to worth watching is appreciated.
    - The official docker documentation is, in my experience, very good
- ..

## [Where to go from here](https://coderefinery.github.io/reproducible-research/where-to-go/)

---

## Sep 29 - Day 4 afternoon - [Social coding](https://coderefinery.github.io/social-coding/)

## [Social coding](https://coderefinery.github.io/social-coding/social-coding/)

## Questions to the audience
### Question 1: Why would I want to share my scripts/code/data?

**Choose many**. Vote by adding an `o` character:

- A: Easier to find and reproduce (scientific reproducibility)
  - votes:ooooooooooo

- B: More trustworthy: others can verify correctness and find and report bugs
  - votes:oooooooooo

- C: Enables others to build on top of your code
     (derivative work, provided the license allows it)
  - votes:ooooooo

- D: Others can submit features/improvements
  - votes:ooooo

- E: Others can help fixing bugs
  - votes:oooo

- F: Many tools and apps are free for open source, so no financial cost for this
     (GitHub, GitLab, Appveyor, Read the Docs)
  - votes:ooo

- G: Good for your CV: you can show what you have built
  - votes:oooooooooooo

- H: Discourages competitors. If others can't build on your work,
     they will make competing work
  - votes:

- I: When publicly shared, usually we time-stamp or set a version,
     so it is easier to refer to a specific version
  - votes:oooo

- J: You can reuse your own code later after change of job or affiliation
  - votes:ooooooooo

- K: It encourages me to code properly from the start
  - votes:ooooooooo


### Question 2: The most concerning thing for me, If I share my software now

**Choose one**. Vote by adding an `o` character:

- A: It will be scooped (stolen) by someone else
  - votes:ooo

- B: It will expose my "ugly code"
  - votes:oooooooo

- C: Others may find bugs and mistakes. What if the algorithm is wrong?
  - votes:ooo

- D: I will get too many questions, I do not have time for that
  - votes:o

- E: Losing control over the direction of the project
  - votes:o

- F: Low quality copies will appear
  - votes:oo

- G: I won't be able to sell this later. Someone else will make money from it
  - votes:oo

- H: It is too early, I am just prototyping, I will write version to distribute later
  - votes:ooooooooo

- I: Worried about licensing and legal matters, as they are very complicated
  - votes:ooooo


### Question 3: Why is software often treated differently from papers?

Free-form answers:
- Software is constantly being updated and upgraded while paper needs to cover large topic at once
- Its harder to check someones code than read someones paper, and in my experience people are less rigorous about checking someone elses code than someone elses writing
    - code is more difficult for more ppl
    - but code can be checked automatically and rigorously (does it work or not?), while a paper can't (ok, AI agents aside for a moment)
        - yes and hopefully these tools will become more easy to use 
- historical reasons; in the past a lot of software was behind locked doors +1
- In most research, the code is not the end goal but just a tool to study something, while the paper contains the discussion and conclussions (i.e., the core of the research) +1
- Software needs to be maintained after publishing
- The environment around the code (dependences etc.) might change over time, paper remains the same.
- Many researchers are satisfied with just outlining their sources and methods in their published manuscripts as a minimum threshold for transparency (i guess), but it inhibits reproducibility and building on top of that work by other researchers
- not widely known that software/code can be considered as research output as such (getting published, eg. Journal Open Source Software) 


### Question 4: When you find a repository with code/library you would like to reuse, what are the things you look at to decide whether you use it?

Free-form answers:
- License +4
- dependencies +1
- does AI know about it?
- documentation +5
- has it got automated tests? +1
- tests & tests coverage
- maintenance frequency (GitHub insights)
  - are there a lot of issues opened that nobody bothered to fix?
- LFXInsights or similar, if available
- last stable release date
- GitHub star count :star: 
- .
---

Your questions here: 
- How about citing packages within your article. For example for tidyverse, is it enough to cite tidyverse as a package collection or should cite exactly each package used.
    - Usually software packages state how they want to be cited. That's usually a safe way to go. +1
    - what about this: https://citation-file-format.github.io/? 
        - The easier/clearer you can make, it the better
        - I think that is different from what was asked above (if I understood correctly). That file is good to add to your own code, or search for it in the software/packages you are using. That is perfectly okay, but I think the question was more towards how to cite when I am using a collection of packages, i.e., too many packages. I am not sure about tidyverse in particular, but those collections should include citing instructions that already consider the individual packages they carry (or directly refer you to their individual citing guide).
        - In the case of tidyverse, they have the following guideline: https://tidyverse.org/blog/2019/11/tidyverse-1-3-0/#citing-the-tidyverse. They say "We generally recommend citing the tidyverse paper instead of citing individual packages", but that is because all the authors of those packages are included as authors in the tidyverse package too. They have a really nice explanation there in line with this discussion :)
            
- When we talk about openly sharing code for reproducibility, how should we think about the environmental cost of storing and maintaining all of this data online? Even very small projects can create repositories, environment files, versions, backups, and duplicated dependencies. Is there any guidance on balancing open and reproducible research with reducing unnecessary digital storage and computing footprint? :+1: 
    - My opinion: if some research value is worth, then it is also worth spending the resources to make it reprodcible. Small repositories will also use less space and less resources.
    - as an extra comment, reproducibility reduces the amount of resources used in many cases in my experience, since it promotes reusability. I agree that initiality it involves extra resources, but avoids redundancy of files in the long run (i.e., you end up reusing them in your own projects and other people will use yours instead of creating very similar ones). This of course depends a lot on how well it is carried out and the complexity of the project.

- What about dependencies of cited packages? Should those also be acknoledged in some way? 
    - It is good practice to add an environment file showing all dependencies. Your tool then figures out the other dependencies for you. Unless there is something specific about them, probably no need to highlight them otherwise.
    - All licences that inherited should be acknowledged.  
        - But that will be really difficult sometimes. Especially for non-python dependencies that are not listed in normal requirement files. 


## [Software licensing](https://coderefinery.github.io/social-coding/software-licensing/)

Your questions here: 
- Do copyleft license limitations apply when "using/reusing", or only when distributing software? With a copyleft license I always need to make the code available when I distribute the software, right? Is this correct?
    - For your poersonal use it is OK. You may use Copyleft software with your MIT code. The issue ia when you distributing 
- If a particular AI-prompt falls under copyright, does the text produced by AI with that prompt fall under copyright even without human modification? (for example, documentation texts created this way) 
    - My understanding is that GenAI output is not copyrightable, since it lacks human authorship. https://fsfe.org/news/2026/news-20260825-01.html Maybe there will be changes to this at some point.
        - i think there's been discussion on certain amount/type of editing -> makes it original enough to be copyrighted by the person; not tested in courts yet, probably..
- If I use a library as a dependency (`import somelib` in my code and `somelib` in requirements.txt) and is is "strong copyleft", does my project need to be strong copyleft too? And with a weak copyleft, this obligation is not there, right? 
    - Basically yes if you are planning to distribute your software. With weak copyleft that obligation stays only for the weak-copyleft part. (disclaimer: I am not a lawyer, but I can bet one pizza on this :))


## [License Selection Decision Matrix & Scenario Index](https://coderefinery.github.io/social-coding/software-licensing/#license-selection-decision-matrix-scenario-index)

### Question: How do you work with other's code?

**Choose many**. Vote by adding an `o` character:

- 1. Writing everything yourself
  - votes:ooooooooo

- 2. Implementing a published algorithm 
  - votes:ooooo

- 3. Pasting in a permissive snippet
  - votes:

- 4. Pasting in a copyleft snippet
  - votes:

- 5. Importing or linking a library
  - votes:ooooooooo

- 6. Writing a Dockerfile or .def
  - votes:oo

- 7. Publishing a built image
  - votes:o

- 8. Using Copilot, ChatGPT, Claude, or similar
  - votes:oooooo

- 9. Shipping prompts, weights or datasets
  - votes:o


Your questions continued: 
- Does "Writing everything yourself" include using libraries or not? 
    - Yes, but you do not distribute the libraries you are importing, eg `numpy`
      - thanks!
- What about using AI to improve the reproducibility of your code? You provide de code you built up the old-fashioned way.
    - "it depends", if you are doing lots of refactoring the AI may introduce code someone else has written (and may be copyrighted under a copyleft license) 

> JoinUp Licensing assistant that Sabry is showing: https://interoperable-europe.ec.europa.eu/collection/eupl/solution/licensing-assistant/find-and-compare-software-licenses

- What does the citation.cff file look like?
    - We will come to that (suspence...)
- The linking/import issue applies only if I distribute the binary, right? If I just have the source code on GitHub and list the dependency somewhere, I don't have a problem with that, right?
    - Probably yes, but you e.g. can't easily provide an example website that uses the tool (since it bundles stuff and makes it 'available'). 
      - I expect there might be a difference between the case where the code is run server-side vs. client side in the browser? 
- Enricos comment about adding an issue/comment to the lecture: https://github.com/coderefinery/social-coding/issues


## [Software citation](https://coderefinery.github.io/social-coding/software-citation/)


## Feedback for Day 4 of CodeRefinery workshop

:::success
- Today, we covered everything in the schedule: We looked at different levels of reproducible research, from organizing your files, to recording dependencies and the computing environment. 
- In the afternoon we talked about software licensing and citation . Tomorrow we will look at **code documentation** in the morning (why and how you can document your code with in-code comments to beautiful websites) and **Responsible use of generative AI in assisted coding**.
- If you would like to try out any of todays demos or tomorrow the documentation tool , please note that you will need some tools installed, you can follow the [installation instructions for Conda]((https://coderefinery.github.io/installation/conda/) to get them.
- Twitch will store the recording of today for 7 days, and we will try to place it on YouTube by the time that expires`

- This is the only way we currently collect direct workshop feedback, please take a moment to let us know how it went :) The feedback is for both morning and afternoon sessions. 
:::

### Today was (vote (add an `o`) for all that apply):
too fast:
too slow:
right speed:ooooo
too slow sometimes, too fast other times:oo
too advanced:ooo
too basic:o
right level:oo
I will use what I learned today:ooooooo
I would recommend today to others:ooooooo
I would not recommend today to others:


### One good thing about today:
- As a complete beginner at github, i learned stuff that i would never even have thought to google, and that are definitely very important for my work! I had never looked at a license file before and it was really interesting (and important) to learn about
- confirmation that the licence world really is horror...
    - no im really convinced i'll never get those (ha!)
      - I'm overwhelmed too and I just think "I'll go GPL everywhere"
      - I though MIT is the only option (ha again)
        - the simplest for sure (but if you "reuse" GPL somehow then you can't use MIT...) 
            - not what our institutes lawyers said...
              - "reuse" here is a general term that should be changed to something more specific, and it that case the GPL obligations apply
        - oh right... so: horror!  but still - this WAS useful information, sort of getting an idea of all that is unknown 
- Great learnings from today again. Thanks!
- complex issues today, but great to have an overview now and links for further reading!

### One thing to improve for next time:
- I feel that there was a big jump from the level needed for the last sessions (which I could follow all of) to today, where some went over my head because im new-ish to sharing my code
  - Thank you! which bits were difficult? Could you mention even just some keywords?
      - yes! containers were something that seemed like it would be useful for me but went over my head a bit, also the snakemake stuff (good that I know what it is and when it would help me, but I could not follow along easily), the licensing stuff was fine in level -idk if maybe it helps to make it more interactive I definitely learn better when doing it myself +1
      - to add to the point above, having some time reserved for carrying out the demos ourselves would have been valuable (similar to the exercises in week 1) +1
          - Yes, some time ago we opted for demos instead of exercises, because of time. The course day is already long and for many participants it was not possible to run the exercises in the time that the instructors are now showing it. But thank you for the feedback, we may reconsider this and bring back some exercises and adapted timing. Any suggestions are welcome :) 
            - Please also take the opportunity to go through the demo/exercises by yourself afterwards.  
    - docker 101 needed, how to get even started with those, very useful these containers
        - some of our partners (and many others) run these kind of courses, see some links to their training offering in our [workshop outro](https://github.com/coderefinery/workshop-outro#ask-for-local-support-from-partners)
