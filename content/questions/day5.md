+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 5"
+++

This document contains the shared notes activities, some direct identifiers have been removed.

# Day 5 - 30/9/2026

### Icebreakers


:::info
Videos from past days are now on  [**CodeRefinery YouTube channel**](https://www.youtube.com/playlist?list=PLM0WX67i-k9s) !
:::

### Icebreaker

What (or where) will you (or do you think you'll have) for your next meal?
- Sushi!
- Mushrooms
- Risotto too!
- Whatever the staff restaurant has.
- potatoes
- In a restaurant, some fancy meal today
- I only think about smoked salmon right now. 
- 

How do you take notes?
- A gigantic google doc with snippets of things I should not forget, new stuff on top.
- Post-its for short term things
- Pen and paper mostly
- iPhone notes app and emails to myself (I know this is suboptimal)
- I'm especially interesed in how people use "notes apps" +1
- self-hosted NextCloud notes
- Hand written notes (I write literally everywhere), post-its, I try desperately to keep tracking in one single space using Notes on Mac, but generally speaking it's not kind of working. I was brainstorming on AI agents that would be able to track my notes, but it's still a work in progress thing. - Rarely I tried to record my voice; I also send notes to myself via WhatsApp too. Wild.There is still not winning strategy tracking notes/keeping a useful documentation. 
- a bunch of markdown notes and Obsidian to visualize it (currently working on how to self-host those :)
- Notepad or MS Word
- Obsidian


### Lesson motivation

Is project documentation important? Why?
- Documentation is fundamental, all I learned was by reading the manuals. Kudos to R packages docs.
- For communication between different users, track of progress etc
- It is very useful for my future self so that when I go back to a folder I see where I was, what needs to be done next, and so on...
- very important to self, forgetting everything if not for notes (also saves head energy)
- All I know is that documentation is a pure nightmare for corporations, for some reason. Without making names...
- Important, sure, there is so much things and work ongoing that you can come back to Docs later.



How would you describe a useful documentation?
- Clearly and logically structured, understandable for people not familiar with the project +1
- it is easy to find what you are looking for
- Usually divided between background and working documents, relevant literature, and (as I work with EU projects) divided among different working packages or WPs.. 
- the documentation is findable by everyone
- for long documentations for large projects: readable by AI; putting all our documentation into NoteBookLM is what helped people here the most
    - What makes documentation readable (or not) by AI?
        - I do it as pure markdown documents. Inline did not work that well. But for me it is 1000+ pdf pages of documentation.
        - Ideally, accessible via API, exportable as plaintext/JSON/XML/structured output
- **searchable**, I need to be able to find a specific thing I am looking for within +2
- not hiding information, not dumbing it down, even for sake of simplicity
- Structured enought well, if references that helps.
- Has typical workflow examples, much better to start from something standard than from scratch
- From my personal point of view documentation should be not verbose to begin with. Concise, good formatting, perhaps we should rethink the design of documentation. I am reading very good points, indeed. [Most likely AI will handle all available notes globally in the future, but how do we protect IP (intellectual property) then? :-)]. PS: I have strong visual memory, so I'd love to have more visualization patterns I'd guess. 
- 
How can you motivate your colleagues to contribute to the documentation?
- Give them a badly documented one to work with themselves +1
- Try to reproduce their workflow and ask for the missing elements
- Checkbox in github/gitlab for new merges that documentation is added/adapted
- Encourage them to do it, as it is important later on.
- Very good question. Documentation lacks ownership and incentives :-) At least for corporations or big institutions, they should quantify the cost of lost time (it's huge annually!).
    -  You can suggest turning it into a paper (ex., JOSS - journal of open source software), maybe then there is more incentive to work on it?
    -  Loss of time by writing the documentation or loss of time from not having a good documentation?


What should a good documentation look like?
- It should look like other good documentations, it should be familiar enough to be able to navigate even in an unfamiliar project +1
- It should look remunerative (Financial ROI)



## Other questions 

- do you speak? i don't hear anything +1+1
        now i can hear

- Now we hear!! +1
    - Great!
- Only now we hear
    - Good :) 

- Can you help to maintain tunneling with liscense server?
    - If RSEs can help with that? It depends, sometimes yes, sometimes it depends on those who manage the license server (e.g. IT). If you are at Aalto and have these type of issues, please join our daily zoom garage.
    
- Can we save this page? This discussiona had many inputs that I would like to continue brainstorming on. 
    - The notes will be archieved and accessible on the Coderefinery page (https://coderefinery.github.io/2026-09-22-workshop/communication/)
- What are the names of the lecturers again please? (Responsible use of generative AI in assisted coding). 
- Do we need real-time coding? (for the training cut-off dates issue, which is a very common limitation). We need real-time everything basically.
- 

## How to document your research software

- what does sphinx-autodoc2/Sphinx AutoAPI do? 
    - Sphinx AutoAPI and sphinx-autodoc2 are the Sphinx extenctions that can generate API documentation for python packages. It basically reads your code and turns the comments into a documentation website. Not sure how much information you want, there is a lot on Sphinx documentation page :)
        - yes, I already took a look but since I've never heard about these, wanted a human elementary summary. Thanks.

::: info
### Break untill XX:00
:::

## Sphinx and Markdown

:::warning
### Exercise until XX:15
Exercise/follow along link: https://coderefinery.github.io/documentation/sphinx/#exercise-setting-up-a-sphinx-project
:::

- ...I just only installed Miniforge3
    - :clap:
- So I could have my webpage with username.github.io?
     - Exactly! This is why we host coderefinery.github.io like this so that each repository has its own mini-website.
     - A good template for researchers: https://github.com/academicpages/academicpages.github.io
     - There is also [GitLab pages](https://docs.gitlab.com/user/project/pages/)  and even [Codeberg pages](https://docs.codeberg.org/codeberg-pages/) if you want your git-based website to be in the EU.
- Is GitLab free of charge?
    - Free for individual users (limits on storage)


:::warning
## Lunch break untill XX:00 (14:00 Finnish time)
:::

## Responsible use of generative AI in assisted coding
https://coderefinery.github.io/coding-with-ai/ 
 
- How do you use AI? I "hate" CSS so I am very happy that generative AI can take care of that :)
    - To do stuffs that (1) I can judge the output or (2) I don't care much about the output (my personal website for example)
- ...Everybody use AI but not everybody say that. I mean in the papers among the scientists. Students are writing their PhD in perfect language with chaGpt. That is the question. Themselves or not themselves
- GPT doesn't create something new it borrows from what he has gained from other people, so called plagiarismus))
    - +1
    - -1
    - For what? If you think of anyone who uses a search engine as an AI user, then yes, since this is pretty much impossible to avoid.
        - Maybe some, but they are then not writing a PhD thesis (themselves).
            -  That is the question: if one chinease write his PhD thesis in perfect german and the supervisor said: he did it not himself, i know his level of language. Is it plagiarismus or not? Even not plagiarismus but somehow cheating from his point of view.
                - One issue is that "AI" can be many things and General Purpose AI Models (like llms) can do many things: a translation is not necessarily plagiarism (plagiarism is using someone else's work without acknowledging it). It becomes plagiarism when the statements that are written (with or without AI) claim originality when they are actually taken from other's work without citing it. 
    - Regarding writing with AI, there are several approaches to it too. If directly using it to generate text, then it is plagiarism as pointed out above. If used afterwards to improve the grammar and language in general, then it can be fair use but of course the line is not always clear. I personally like to use it to discuss specific word choices, since I am not a native English speaker and don't know the nuances of the language (akin to asking advice to a native speaker, without giving my actual text). This is not a productive application of AI though, but I feel that passing the actual text kills a lot of my creativity (of course LLMs will generate a text with a perfect English compared to my writing, but that is not my goal). 
    - sure, but then the AI written english, even if you simply ask it to "finetune" your work, ends up sounding so mechanical. Very soon we will have thousands of work that sounds exactly the same! I personally find it very mechanical and monotenous +1
        - definitely agree! My point was that there are ways to find a balance, but they are not so efficient (meaning people need to be willing to put the time, which usually goes against the motivation of using AI in the first case)
        - Yes! and i think that is the issue. i feel like we have lost the patience to stare at a blank word document and think before writing something. it is so easy to ask AI to generate something +1
            - I guess it became a question of whether you like writing (so you prefer doing it yourself first) or not (then AI is very tempting)
    - Great points and perspectives everyone. Yesterday we mentioned "is it plagiarism / IPR infringement if we reuse print("hello world")"? I think what everyone is trying to figure out where the line is between "fair use" (in the USA sense, we have a comment in yesterday's materials: https://coderefinery.github.io/social-coding/software-licensing/) and "IPR infrengment"... and unfortunately court cases are not really taking a clear stance on this.
- What tools do instructors use for AI coding agents?
    - A bit of everything (claude code, codex, pi). I have tried also local models like Qwen 3.8 which we have at Aalto and it works quite well.
    - This can become a full-day session ...
    - chatgpt, github co-pilot. 
- I am using AIs with subscription through my employer due to safety issues. As these AIs are approved by the employer, I feel more confident there will be no sensitive data leaks, as well as we get support from the employer regarding its usage. We started with CoPilot but due to intensive coding demands at our firm -> moved to Claude. I like it ... :) / Thanks for the warning. I am definitely staying on the safe side. Luckily I am not doing high level coding nor working with legally sensitive data; more like we have a lot of data due to long-term monitoring programs...
    - Anthropic has had security issues in the past. If your employer believes their security assurances are good enough for their purposes than that is their responsibility. Depending on what you mean by "sensitive" data, I would still be careful what you share with them.
        - Unfortunately every provider of frontier LLMs has had one (or more) security breaches.... it seems that they are not that good when it comes to security. :)

## Exercise XX:35 - explore code generation with a chatbot
https://coderefinery.github.io/coding-with-ai/introduction/
(scroll to the bottom)
:::success
 Go to https://duck.ai (no account needed) and try the following:
Ask: “Write a Python function to calculate the standard deviation of a list”
Look at the response. Does it:
- Use a built-in library or implement from scratch?
- Handle edge-cases (empty list, single element)?
- Include documentation?
Now ask: “What assumptions does this code make? What could go wrong?”
Finally, ask: “How would you test this function to ensure it’s correct?”
Share your reflection in the collaborative note document.  
:::

- I did it twice and got two completely different implementations :D
    - EH. I tried the same, indeed. At least the math looks correct'
    - I got the same thing twice 
- For me it did not use a builtin library. Which one should it be?
    - statistics.pstdev(values) would do it as a built in solution 
    - in my case, it didn't use it but it suggested it afterwards as an alternative
        - did you have to ask it? I sometimes need to mention "I want to reuse built in functions as much as possible and limit the amount of code" otherwise it is so verbose...
        - I didn't ask for it, but when I ask for the assumptions and what could go wrong, it added a last comment saying that for production code that builtin method was a good alternative. Interesting how different the answers can be with same questions!
- Can you change the language model it uses in duck.ai?
    - I think that only when you start a new chat you can pick a certain language model. So in different chats with different models you can try the same prompt for example. Note that after a while it goes to "you have used all your free credits for today"

- Small things matter, so it’s important to check your work carefully while coding. Even a small functions can go wrong if the input is empty, the data is bad, or the assumtions are wrong. Testing is improtant part of the code writing, and good testing plan or aims targeted are important. 
- I wonder if the check it did is real?
    - This is a very important point: some LLMs are not connected to tools (e.g. running a python command and show the output) but they just generate the results based on the LLM probabilities. I guess you might have come across that when you ask "how many Rs are in strawberry" it says (or used to say) 2. I am not sure if duck.ai runs python code snippets, I think not.

- I don't understand how can we pick another model (or if it is even possible with this tier)? Never mind, you cannot. You must start a new chat. 
    - Yeah I also had to start a new chat, you can't change mid-chat 
    - Yes, since duckduckgo is just routing your queries to another service, you can't change the model mid-chat
    - Being locked into one model is likely because different models tend to use slightly different API methods, and often enough there is no 1:1 translation between specific APIs. E.g. some APIs have features that aren't implemented by others (like API specific tool_calls (web-search)), so duckduckgo decided not to go to the trouble to translate between them and locks the model for eahc conversation. 
        - Thanks. I think that big AI should hire the entire global population in order to boost AI literacy.
- What models did you guys pick? I started with GPT 5.6 Luna. 
    - GOod question. If it's just a one liner (my use of duck.ai) it does not matter much, but with more complex things I have seen that gpt-oss tends to hallucinate. Nice that they have Mistral which is a European alternative (but not the best for coding)
- Can AI assistants pick themselves the best model based on the prompt? 
    - Some tools (like claude code) do "model routing". I am unsure how common this is.
    - Essentially it's an additional call to a model asking what's probably a good model for the following task and then giving descriptions of the models. Can be useful to save some costs for low effort requests, but can also backfire. 
- This time I tested Claude Haiku 4.5 and I modified settings. 
    - was it better? 
        - Not sure. This model sounds insecure. Strange. 
            - :D like emotionally insecure or just not-secure in the cybersecurity sense
                - It asked questions back that it should have been able to determine quite easily on its own. Hm.
                    - I see. Well at least it asked instead of assuming :) 
                        - Safety first. 

### Exercises with chatbots until xx:00 (we will have a short break after that)

https://coderefinery.github.io/coding-with-ai/scenario-full-control/#exercises

- I get a very long function when I ask to do the validation also
    - Yes this is one thing I don't like because it can take longer to review it rather than what I would have done myself with good documentation and a bit of patience. I am unsure how some are "vibe coding" everything (companies in production environments) and ... hope for the best? or do they spend days reviewing all those thousands of lines of code?
        - If you mostly vibe-code front-ends a lot of the risk is pushed towards the user side of things, as bugs tend to leak individual credentials instead of access to the system db. 

- I am not sure if I defined the problem properly (as I dont know Python?), however I get an answer that the code crashes due to len(data)=0 :D 
    - same +1
    - Well, that "crash" could be intentional during Validation. Failing Validation commonly raises a "ValidationError " which makes the code error out, but that is actually expected.
    - So it tells you what error it expects when you would try to run the code? Is that what you asked for?
- also for problem 2, loads of code... I am not sure if it is right or wrong
    - As a suggestion: Ask it to use pydantic to define the schema and have pydantic do the validation. The code should get cleaner, at the cost of introducing a dependency
        - Thanks for the tip! But then I would need to understand what pydantic does to review the code :) (I am R person with very basic python skills)
- ..

:::success
## Break until xx:12
Remember to stretch your muscles and drink some water/tea/... :)
:::

Your favourite IDE / tools?
- VS code with integrated Github Copilot+
- VS code, but I never tried it with AI. How do you enable it?
    - You install an extension (I used github copilot plugin) and then when you log in with your github account you have some free credits (but not too many). I am unsure though of which files from the local folders are sent to the remote provider, so I don't use it for research purposes.
        - The instructors just mentioned a bit of this :)
        - There are also some instructions in the docs if you want to start using github copilot: https://coderefinery.github.io/coding-with-ai/scenario-ide-integration/#setting-up-github-copilot
- Did one of the instructors mention SETH? 
    - I think he meant "Zed" but I will ask 
        - Thank you. I accidentally cancelled something, sorry! https://zed.dev/
    - What are the advantages of using Zed vs. other editors? Maybe they already mentioned it but I didn't hear it. Thanks :D
        - Good question, I will raise it to the instructor since he is a user. 
             - AM: Some advantages - the AI "plugin" comes by default and fully open source, it supports a protocol called ACP (Agent Communication Protocol), also a bonus written in Rust. VSCodium the fully open version of VsCode cannot run GitHub Copilot for example.
                 - Thanks! I will check it, sounds promising. I never got to start using VScode, sounds like a nice alternative
                 
- I used OpenClaw/InstaClaw at some point. I need a proper roadmap to start seriously testing AI agents for different purposes and use cases. Any advice is more than welcome.
    - I wish for similar roadmaps or systematic tests. I feel that people just catch the latest hyped tool/model and there is nothing systematic like same prompt over the years -> is the output quality better? (or maybe there is but I have no idea, please share links if you know)
    
- I started using Claude Code, but then when I realised my institution started offering an API endpoint with open weight models I started using OpenCode connected to it. But I don't use these tools as a "project manager", I use them as the pair programmer none of my colleagues has the patience or the time to be. Also: I have an editor open at the same time 
    - Very interesting! Thanks for sharing. Promoting pair programming would actually be really good rather than just "delegate everything" +1 +1
    - Can you ellaborate a little on what you mean by pair programmer? Is it that you code at the same time, or you divide the tasks or ...?
      - It's the practice of sitting at the keyboard with another person and coding together, thinking through the problem together and throwing ideas at each other (at the first year in Uni we were doing this without knowing it had a proper name, we just thought that there were no computers for everyone)
          - Oh I see, so like an ongoing discussion about the code. Thanks!
            - It's kind of an "alternative" to code reviews. You get work done quicker than alone and you have two people that know the code well isntead of one. But it can be very tiring and a bit less efficient 
- Naive question, is there any advantage of using English vs my native language (non-English) when using AI?
  - It has been reported that e.g. in German some models tend to use ~50% more tokens (don't remember the exact number). I've also heard that some chinese models might work better in Chinese. But I can't tell how solid the "evidence" for this is.
  - Another rumor from the internet, logographic languages (like chinese) are more compressed and so work better, but... well you need to know Chinese. :)
    - What about translating your prompts with AI? :-)
        - You have a good topic for a research paper. Thanks us in the acknowledgments :)
  - Most languages are underrepresented, isn't it? English monopoly I'd guess.  
  - Thanks everybody for the answers, very interesting :D

- A good idea for any government would be to purchase AI memberships (i.e. unemployed, disadvantaged categories, etc) to boost AI literacy and favor the transition to post-labor economics. I always insist on this side because I still don't see any proper policy going on atm. This is paramount. 
  - ~~Many institutions are doing this, in Europe.~~ Many institutions, AFAIK, are offering some self-hosted open-weight models. 
      - Good to know. Awesome. We need to do more tho (evidently).
        - By the way: I am both astonished and apalled looking at what AI can do. Are we going to really transition to post-labor economics? Can we really trust these systems? Do they really work well enough that we can forget about them? hmmm...
            - we have a thread in coderefinery zulip chat about this... about 10000 lines long :D Welcome to zulip chat if you wan to rant, I mean, discuss https://coderefinery.github.io/manuals/chat/
                - I want to join, defo.
                - Some literature https://www.goodreads.com/en/book/show/59801798-blood-in-the-machine https://thecon.ai/
    - (apologies for the drift of topic, but yes it is shocking that because *everyone* uses whatsapp, then Meta can just push their AI chatbot to all whatsapp users, while I would rather have a local government or EU commission to push such app in everyones phone if it must happen....)
    - Purchasing services on a massive scale from foreign companies that have a questionable track record when it comes to ethics or adherence to local laws probably raises questions of sovereignty.
        - Indeed. And then they partner with microsoft or meta :')
        - It could be "cheaper" (and less "committal") in the short terms to make agreements with "BigAI" than to buy your infrastructure and host open weight models. 
            - In the short term certainly, since they are currently still heavily subsidizing AI use. In the long term you give them a lot of data, which widens the gap between closed and open models, which would make you increasingly dependent on them.
               - But open weight models can be order of magnitude cheaper to use while at the same time being good enough for most tasks (I get decent work done with DSv4.0 flash)
               - I am not sure the interaction with the users is (like RLHR (?)) that effective at improving the models (it seems very efficient at stealing ideas from the scientific communities though). 
               - 

- We should probably discuss about datasets at some point. 
    - Like which data can be used with AI tools? 
        - Yes, absolutely. And especially how can we improve the quality of datasets in the future. This is from the perspective of new AI actors in the industry (in EU). We discuss a lot nowadays about Sovereign AI in Europe. 
            - GOod point, I can raise this in the end with the instructors.
            - Yes there are two aspects -> using AI for improving dataset quality, but also giving datasets to AI (especially even if you do not want to give those data to those companies training AI models). 
- I am mind blown that the AI agent did all that by itself. Do we even need coders anymore???
    - Well, you always need human in the loop, for accountability ;) 
        - Insert Homer Simpson's keyboard bird meme (pressing the "Y" key in repeat)
    - Code is read 100x or more than it is written, at least the serious projects. Also reviewing and verifying need some basic skills, at least :)
    - The instructors will go now through some reasons why humans are still needed in the loop :) plus other reasons like the accountability point mentioned above. Reviewing code made by AI requires certain coding knowledge, and debugging is getting more and more convoluted so if something goes wrong, you cannot have a "non-coder" simply looking at it. Another AI agent can take this role, but they are not infalible.
    - AI is intelligence. Intelligence alone can't solve all the problems: any intelligent system (be it human or AI) needs data to produce useful results. AI can't (yet) go to the world and ask the important questions or run experiments. The role of a software engineer is also to do "requirement" engineering, and even ASI would not be able to do that without being it much more integrated in all humans activities than it is today. It's still your responsibility and duty to at least state the requirements in a consistent way (and define clear testing goals)
    - Other good reason is, in the case of scientific code, the science can get very entangled with the code (which is why many scientist learn coding in the first case). AI doesn't perform so good (for now) without continuous feedback and new input/pair coding in those cases, at least from my experience. This relates with the comment above about intelligence, just wanted to add a comment from the perspective of a scientist instead of an RSE.
- Will we need new types of insurances for AI agents in the near future? Considering all current and latests events...They
  - Interesting idea. I guess you just gave some new ideas to insurance companies if they are reading this. 
      - I want the royalties lol
          - Ideas cannot be copyrighted sorry :)  
            - That's the greatest challenge ever for the AIs era. How do we truly protect human intellectual property?
                - can we even protect it at this point? :') But I definitely agree
                     - We should. But the question is technically how? Let's pay people for thinking? :-)
                         - Love this idea, 100% :)
                         - Not sure this is true. Human intellectual property was already lost pretty much entirely to some large companies.
                             - Exactly. I have some ideas.... :-))
                             
    - Given that some AI experts think that there's a 10% chance that AI will wipe humanity, which insurance company will insure it? 
        - Yes and the frontiers AI companies are committing all sorts of breaches and not paying for any damages...
          - It's also a huge publicity for them. 
            - Hype apart, I bet we will need new types of insurances for AI infrastructures, AI agents, next-level ASI, you name it. Clearly. (Especially GovAI/GovTech).
            


- ...
- ...


## Feedback for Day 5 of CodeRefinery workshop

:::success
In the morning we covered documentation and how to publish github pages and in the afternoon we looked at responsible coding with AI. Thank you for the active discussions. The "AI lesson" is still work in progress, so any useful comment will help us improving it. Please answer the polls and questions below.
:::

### Today was (vote for all that apply):
too fast:o
too slow:
right speed:ooo
too slow sometimes, too fast other times:o
too advanced:o
too basic:
right level:oooo
I will use what I learned today:oooooo
I would recommend today to others:ooooooo
I would not recommend today to others:oo


### One good thing about today:
- Great learniing again - thanks!
- Very interesting topics, indeed. I enjoyed a lot. 


### One thing to improve for next time:
- Sometimes Less is More.+1 
- It would be good to have more q & a with the instructors
- If we focus on Q&A and getting further insights from the lecturers, we kind of miss the focus on the webinar itself. There is so much to be discussed, let alone to be learned that we risk to completely lose the target so to say. Maybe, we should have Q&A at specific times. But I like this kind of format that allows you to interact freely. 



### Any other feedback? General questions?
- Personally, we should probably use this platform to discuss real-life projects and build teams. Never say never. Everything is so fragmented in this digital ecosystem somehow. We never get things done. We never reach the goal after all.
 
- I am obsessed by Sovereign AI and tackling bureaucracy, to the point I suggested to fully delegate all bureaucratic tasks to AI, creating an entire infrastructure. But this ideas is perhaps way too grandiose. I need an audience and some feedback to reassess further. Theoretically, who needs bureaucracy? Who loves bureacracy? What's the purpose of bureacracy? Can't AI be a better Bureau at least? Faster, less biased on a long-term basis, certainly more efficient (24h/365days) and the majority of people working in public bureaus hate their jobs and hate citizens frankly speaking (this is a fact). So why not transition them to activities they actually love? We - the people/the citizens - would finally get better services and in a fraction of seconds potentially. Not in months or years or decades. Think about it. 

- I believe in what I call the democratization of AI --> access to supercomputers and hybrid systems should be a human right. That's the only way to avoid elite capture. More to come, stay tuned. :-)

- Last but not least, I truly believe we don't have enough futurists and visionary leaders to bring us into a bright post-labor economics era. We don't need doomerists or apocalyptic theories or extreme polarization to discuss our predictions. But change is inevitable. Robots will live with us, decisions will be taken by AI systems. There are thousands of papers out there, an infinite amout of documentation, interviews, YT material that shows why we will transition to this new way of living. Check David Shapiro on YT and give me a honest feedback. It was great to be here. See you tomorrow!


