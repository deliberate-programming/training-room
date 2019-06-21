# Deliberate Programming Training Room

If you want to try out Deliberate Programming for yourself this is your starting point.

0. Make sure, the .NET Framework or the Mono runtime are installed on your machine. On Windows that should be the case anyway, but on Mac/Linux you might want to check by running the `mono` command in a shell window. See [here](https://www.mono-project.com/docs/getting-started/install/linux/) for installation instructions for Linux and [here](https://www.mono-project.com/docs/getting-started/install/mac/) for macOS in case you're missing Mono.
1. Clone this repository
2. Run below tests to check if the tool is working correctly for you.


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




## Prepare

Copy this contents of this folder to the root of your Git repo (or the root of the folder tree you're working under).

Then check that everything is working by first running this test inside the folder in a console/terminal/bash window:

MAC/LINUX
---------
mono repeat.exe 5 bash -c ./hello.sh

WINDOWS
-------
repeat.exe 5 cmd.exe /c .\hello.bat

The output should be a "hello, world!" message appearing every 5 seconds.


## Use

To actually use repeat.exe to automatically commit changes you need to do the following:

1. Open a console/terminal/bash window on the parent folder, the root of your repo/working tree.
2. Start auto committing like this:

MAC/LINUX
---------
mono .deliberate-programming/repeat.exe 60 bash -c .deliberate-programming/dp-commit.sh

WINDOWS
-------
mono .deliberate-programming\repeat.exe 60 cmd.exe /c .deliberate-programming\dp-commit.bat


If you like, do a quick test by first running repeat.exe with a period of 5 seconds instead of 60.


