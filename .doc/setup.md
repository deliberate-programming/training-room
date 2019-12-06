# Setup
#### 1. Get .NET Core
In order to use the DProg tooling you need to have the .NET Core framework installed. You can [download it for free from Microsoft](https://dotnet.microsoft.com/download) for your operating system.

#### 2. Get this repository
Fork this repository and clone it to your computer. (If you just clone it, you'll not be able to retain any changes by pushing them.)

Alternatively download the ZIP file of the repository and extract it to a DProg root directory in some Git repository of your own. (Or just extract it and run `git init` in the root.)

#### 3. Check the tools
Open a console/shell window on the directory where the `dp-record.*` files are located in your repository.

Run the `dp-record` script for your operating system like this:

* Windows: `dp-record.bat 5`
* Linux/macOS: `./dp-record.sh 5`

You should see a message like this:

![](images/tool_check.png)

Now create a text file (e.g. `a.txt`) in the repository and watch what happens in the console/shell window:

![](images/tool_check_change.png)

Your change to the repo automatically got committed. Check the commit log with the tool of your choice:

![](images/tool_check_log.png)

Press `Ctrl-C` to stop the automatic recording.

Please also have a look at the directory `Screenshots` in the root of your repo. That's where `dp-record` automatically saved screenshots taken at the end of every interval.

If you got this far without any errors you're set for your first Deliberate Programming session.

#### 4. Install a visual Git client (optional)
Install a visual Git client. It makes it easier to later go through the automatic commits created during a DProg session. The [GitHub Desktop Client](https://desktop.github.com/) would be a free and simple choice.
