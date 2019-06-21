# Deliberate Programming Training Room

If you want to try out Deliberate Programming for yourself this is your starting point.

### Setup
0. Clone this repository
1. Make sure, the .NET Framework or the Mono runtime are installed on your machine. On Windows that should be the case anyway, but on Mac/Linux you might want to check by running the `mono` command in a shell window. See [here](https://www.mono-project.com/docs/getting-started/install/linux/) for installation instructions for Linux or [here](https://www.mono-project.com/docs/getting-started/install/mac/) for macOS in case you're missing Mono.
2. Run below tests to check if the tool is working correctly for you.
3. Install a visual Git client. It makes it easier to later go through the automatic commits created during a Deliberate Programming session. The [GitHub Desktop Client](https://desktop.github.com/) would be a free and simple choice.


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