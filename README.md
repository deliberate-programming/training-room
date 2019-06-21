# Deliberate Programming Training Room

If you want to try out Deliberate Programming (DProg) for yourself this is your starting point.

Deliberate Programming is about systematically getting better at, well, programming. It's based on Deliberate Practice (DPrac) as described by K. Anders Ericsson for example in [The Role of Deliberate Practice in the Acquisition of Expert Performance](https://graphics8.nytimes.com/images/blogs/freakonomics/pdf/DeliberatePractice%28PsychologicalReview%29.pdf). For a less scientific introduction to DPrac see the articles [here](https://medium.com/the-crossover-cast/deliberate-practice-learn-like-an-expert-cc3114b8a10e) and [here](https://medium.com/the-crossover-cast/get-better-at-anything-6-steps-of-deliberate-practice-19830bfc9460).

What DProg is adding to DPrac is a method to work in a focused way on a certain area of improvement and reflect on the experience. For that purpose DProg is employing some tools for automatic observation of one's progress while working on a task.

* Git serves as the "flight recorder" logging all thoughts materializing in files.
* A small tool called `repeat.exe` is used to trigger Git to record recent file changes.
* Optionally a tool to take periodic screenshots and add them as files to the Git repo.

### Setup
0. Clone this repository
1. Make sure, the .NET Framework or the Mono runtime are installed on your machine. On Windows that should be the case anyway, but on Mac/Linux you might want to check by running the `mono` command in a shell window. See [here](https://www.mono-project.com/docs/getting-started/install/linux/) for installation instructions for Linux or [here](https://www.mono-project.com/docs/getting-started/install/mac/) for macOS in case you're missing Mono.
2. Run below tests to check if the tool is working correctly for you.
3. Install a visual Git client. It makes it easier to later go through the automatic commits created during a Deliberate Programming session. The [GitHub Desktop Client](https://desktop.github.com/) would be a free and simple choice.

Optionally you also can install a tool for taking periodic screenshots. This helps if you should be working in non-text files or draw diagrams visible only on screen (eg. by using an online whiteboard app). [Screenbar](https://apps.apple.com/us/app/screenbar/id1329392611?ls=1) can help you on macOS, or see [here](https://www.guidingtech.com/56099/automatically-take-screenshots-windows-pc/) for option on Windows.

### Deliberate Programming
Deliberate Practice [boils down to](https://medium.com/the-crossover-cast/get-better-at-anything-6-steps-of-deliberate-practice-19830bfc9460):

1. Set specific, realistic goals
2. Break out of your comfort zone
3. Be consistent and persistent
4. Seek feedback

This can be done for any skill/discipline/practice there is: you can practice deliberately playing the violine, dancing, knitting, playing chess, cooking, scuba diving, remembering numbers - or programming.

But programming in special in so far as "seeking feedback" is easier because your practice easily leaves at lot of traces which then can be reflected on.

And Deliberate Programming is special in that it guides you through the practice period and a subsequent reflection. DProg can thus more easily be practiced even without a coach - although getting feedback from a more advanced programmer always in very valuable and should be sought.

#### Choose your area of improvement
You start DProg by choosing an area of programming you want to improve in. That can be the application of a tool, familiarity with a framework, Clean Code principles, or a method like TDD.

#### Determine meaningful metrics
For the chosen area of improvement think of how you'd assess your knowledge, you abilities. What does it take to excell in that area? How could you possibly measure progress?

**Example TDD:**

What makes a developer good at applying TDD to a programming problem? Here are some suggestions:

* TDD requires you to write test code before production code. It's a test-first approach.
* TDD requires test cases to progressively become more "difficult". It's an incremental approach to testing.
* * TDD requires you to switch between writing test code and production code again and again. It's an iterative approach to testing.
* TDD requires you to refactor after you got a test to pass. Remember the TDD rhythm: red-green-**refactor**.
* TDD requires you to write the most simple production code to get the test to pass. Remember the KISS principle. But what is simple? It means at least two things: 1) Future tests don't accidentally are green right away because of excess functionality implemented for an earlier test. 2) All alternative cases in production code are covered by tests written so far.

When reflecting on a TDD task you sure can assess whether you acted more or less true to the above principles/rules. The more you observed them without hesitation, the better you are/have become.

So much for general DPrag. Now for specific DProg.

#### Run a Deliberate Programming session
To actually become better at something you have to act. Work through exercises so it's safe to fail. Apply your knowledge and skills at best - and then ruthlessly assess your performance. This is the DProg tools and process come in.

##### Choose a task
Choose a task to accomplish "under observation" by the DProg tools. You can clone this repo for each task or you can collect several tasks and multiple sessions in a single clone. Go through the above Setup steps at least once, though.

**Example TDD:**

If you want to improve your TDD skills you could start with a simple code kata like [From Roman Numerals](https://ccd-school.de/en/coding-dojo/function-katas/from-roman-numerals/).

Choose a task and then right away start working on it "under observation". The more time is logged by the DProg tools the more material there is to reflect and improve on.

##### Work on your task
To start a DProg session you do the following:

1. Set a timer for how long you want to focus. Experiment with different durations, start with 30 minutes.
2. Open a console/shell window in the root of the clone of this repo.
3. Start `repeat.exe` to log whatever you're doing in the repo with automatic commits.

* Windows: `repeat.exe 60 cmd.exe /c .\dp-commit.bat`
* Linux/macOS: `mono repeat.exe 60 bash -c ./dp-commit.sh`

In case you expect to do work in tools not leading to files stored in the repo, also start the automatic screen capture tool of your choice. Let it store the screen snapshots in some sub-folder in the repo so they get auto-committed, too.

If you like you can commit manually, too, at any time. By that you can insert more information into the commit stream. Maybe after 10 auto-commits you get to a "milestone" and want to document that explicitly. That's great help for you later reflection.

**Important**: **Be sure to save your work on files belonging to your task often** (be the tests, production code, documentation, diagramms and what-not). Maybe there is an auto-save feature in your IDE which stores changes automatically when switching tabs, or just press a keyboard shortcut whenever you stop typing (or at least at the end of every paragraph). **Make this a habit!** Only that way you'll get a fine grained recording of the progress you make.

Once the recording of any changes to your repo has been started work on your task for the set duration. For 30min of work you'll see at most 30 "anonymous" commits in your repo at the end; probably, though, it will be less because you won't be changing files constantly.

If you should feel a bit uneasy, tense because you can't shed the thought of being watched (event though it's you watching yourself), that's normal. It will go away after a while when you get used to working this way. Try not to force anything. Don't make it a competition with yourself.

##### Reflect on your work
Once the time's up stop the logging by pressing `Ctrl-C`. Maybe now's the time to take a little break before you start into the next phase of DProg. So far it has been easy. You were doing familiar stuff: programming.

And then, when you're ready, you come back and go through several passes of reflection:

###### Pass 1: Write a thought log
Go through the commits of the task period, look at which files changed, look at how they changed and write down for every commit what you remember about your thoughts at that time in the process. (Sometimes several commits can be bundled up in one log entry because they are very related.)

Using a visual Git tool makes it easier to scroll through the commits with their files. (Alternatively push your repo to GitHub, for example, and use the online view of your commits. This even has the advantage of allowing you to link to commits in your log.)

Make it an "impersonal" report. Just note obersavations about your thinking process/progress. This is not the time for judgement or musings. This is just a log of your thoughs which led to visible results.

Use a simple .txt/.md file to write this log. And don't "overthink" your entries.


Writing this log should follow the SRP: don't do more than logging your thoughts. Avoid multitasking by switching between different mental levels. Try to be impartial.

At the end take a breath or two, even a short break.

###### Pass 2: Assess your thinking
Once you've compiled your thought log you gover that (maybe in conjunction



## Check all is working well on your Windows machine (.NET Framework)
Open a console window on the repository root and run the following command:

`repeat.exe 5 cmd.exe /c .\hello.bat`

The output should be a "hello, world!" message appearing every 5 seconds.

![](images/hello.png)

If that's working fine, run another the following command to check if everything is working well with Git:

`repeat.exe 5 cmd.exe /c .\dp-commit.bat`

The output should be something like this to show a commit was actually tried.

![](images/dp-commit.png)

## Check all is working well on your Linux/macOS machine (Mono)
Open a shell window on the repository root and run the following command:

`mono repeat.exe 5 bash -c ./hello.sh`

The output should be a "hello, world!" message appearing every 5 seconds.

![](images/hello.png)

If that's working fine, run another the following command to check if everything is working well with Git:

`mono repeat.exe 5 bash -c ./dp-commit.sh`

The output should be something like this to show a commit was actually tried.

![](images/dp-commit.png)