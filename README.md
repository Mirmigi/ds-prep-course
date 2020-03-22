# Data Science Prep Course Repository

Welcome to Data Science Prep Course repository. Here is you'll find all information needed to setup your environment and the
workflow you'll use during the Prep Course.

1. [Initial Setup](#initial-setup)
    1. [Windows Setup](#Windows-Setup)
    1. [Setup _Git_/_GitHub_](#setup-_git__github_)
    1. [Setup your Workspace Repository](#setup-your-workspace-repository)
    1. [Get the Learning Material](#get-the-learning-material)
    1. [Running a Learning Unit](#Running-a-Learning-Unit)
1. [Learning Unit Workflow](#learning-unit-workflow)
1. [Updates to Learning Units](#updates-to-learning-units)
1. [Help](#help)
    1. [Slack Usage](#slack-usage)
    1. [How to Ask For Help](#How-to-Ask-For-Help)
    1. [Other](#other)

## Initial Setup

**IMPORTANT**  
Before the prep-course you will have to complete these instructions, this is 
essential.

Once you complete the setup mark yourself as such on [this spreadsheet](https://docs.google.com/spreadsheets/d/1NDddtliEi8RdGmEogCz2Lz-Yyq3IM6wjYDY1IuR18GI/edit?usp=sharing).
Make sure that you complete the setup by the 30th of March, as the course will begin on that day. If you are struggling to install any of the software to be mentioned below, tell us ASAP! The course by itself will be very intensive, so we do not want you to waste time on the setting up part after the 30th of March!! 

By completing this you will setup and learn about all the tools you'll be
using during the academy. We will also be able to identify any problems in time to figure out a solution.

Don't worry if you can't figure out what some the the commands you will
use do. 
Anything that is important will be explained in more detail during the course.


### Windows Setup

This section deals with setting up either Windows Subsystem for Linux (WSL)
or VMWare. 
If you are using MacOS or Linux you can skip this section.  

If you are using windows 10 we suggest using WSL (see below), if you are using an older Windows version we also support running a virtual linux machine with VMWare.

##### Why do I need to install either WSL or VMware?

Because of the differences in command line syntax between Windows vs Mac OS/Linux, it would be a great challenge for us to support and provide instructions for both Operating Systems. For this reason, we’d ask you to install Windows Subsystem for Linux, or VMware, which would enable you to run Linux command lines inside Windows. Keep in mind that these are simply extensions to your Windows operating system, hence, installing this software will not do any changes on your laptop. It is also quick to do so.
 
If due to some reasons, you cannot install WSL or VMware (e.g. you do not have the admin rights for your computer), you can still join the Prep Course and follow the Learning materials. However, all of our setup instructions and learning materials are created for Mac OS/Linux, and unfortunately we will not be able to provide support on how to do it on Windows.
If you have some doubts/worries, feel free to reach out to us.

#### Windows 10 Setup

Follow [this guide](guides/Windows_Subsystem_for_Linux_Installation_Guide_for_Windows_10.md) if you are running Windows 10.

#### Older Windows Setup 

If you are running an older version of Windows (such as Windows 8 or 7), follow the guide below on running Ubuntu with Windows using VMware Player. You'll be required to download VMware and Ubuntu 18, for that please use the links provided below (not the links provided in the tutorial).
* [VMware download link](https://www.vmware.com/go/getplayer-win)
* [Ubuntu download link](https://ubuntu.com/download/desktop/thank-you?version=18.04.4&architecture=amd64)
* Follow this guide: [How To Run Ubuntu in Windows 7 with VMware Player](https://www.howtogeek.com/howto/11287/how-to-run-ubuntu-in-windows-7-with-vmware-player/)

### MacOS Setup

Some of the steps in the following sections will require _Homebrew_ for MacOS.
Homebrew will make it easier to install software that we will use later on.  
To open the terminal, choose one:
* In Finder <img src='assets/finder.png' alt='Finder' width="4%" height="4%"/>, open the /Applications/Utilities folder, then double-click Terminal.
* By pressing <kbd>cmd</kbd> + <kbd>space</kbd> then type `terminal` and press <kbd>enter</kbd>.

The terminal should now be open:

![](assets/mac_terminal.png)


Copy and paste the following line in the terminal:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
You may be offered to install the _Command Line Developers Tools_ confirm and
once it's finished continue installing Homebrew by pressing <kbd>enter</kbd> again.

### Setup _Git_/_GitHub_

Git is a distributed version-control system for tracking changes in source 
code.  
A repository is where code lives, and the code from the prep course will live in the [ds-prep-course](https://github.com/LDSSA/ds-prep-course) repository, and the learning materials and exercises will be released (made available) in that repository.

#### Install Git

##### Under Ubuntu
Open a terminal (or use one you've already opened) and run:
```bash
sudo apt update && sudo apt upgrade && sudo apt install git
```

##### Under MacOS
```bash
brew install git
```

#### Create a _GitHub_ account

[Sign up](https://github.com/join) for a _GitHub_ account and follow 
instructions.

### Setup your Workspace Repository

The workspace directory/repository is where you will place everything you
are working on.

#### Creating the Workspace

1. Log into _GitHub_
1. Create a new **private** _GitHub_ repository called *ds-prep-workspace*, see 
[Creating a new repository](https://help.github.com/en/articles/creating-a-new-repository). 
1. You need to explicitly select Private - This is your work and nobody else's. 
1. Initialize with a README. 
1. Add a Python `.gitignore`.

![Create Repository](assets/create_repository.png "Create Repository")

#### Cloning the Workspace

* Open a Terminal (or use one you've already opened)
* We're going to have a folder named `projects` where we will keep the repositories we'll be using.
* We're going to use the `mkdir` command to create it, and the `cd` command to enter the folder: 

```bash
mkdir ~/projects
cd ~/projects
```

* You can now clone (retrieve from GitHub) your /ds-prep-workspace repository using the `git clone` command:

```bash
git clone https://github.com/<username>/ds-prep-workspace.git
```

* Now type your git username, then press <kbd>enter</kbd>
* Then type your git password , then press <kbd>enter</kbd>
* You're all set!

### Get the Learning Material

You will be cloning the [ds-prep-course](https://github.com/LDSSA/ds-prep-course) 
repository.
All of the learning material you need will be made available on this repo
as the academy progresses.

1. Open a Terminal (or use one you've already opened)
1. Make sure you're in the right directory (use the `cd` command to enter the `~/projects`)
1. Clone the students repository 
[ds-prep-course](https://github.com/LDSSA/ds-prep-couse)
```bash
cd ~/projects
git clone https://github.com/LDSSA/ds-prep-course.git
```

#### Get the Week 0 Learning Unit

In the `ds-prep-course` repository that you just cloned there is a Week 0
learning unit.
It's used to give instructors guidelines to produce the learning units.
We are also using it to ensure that you are able to run and submit a learning 
unit.

So go ahead and copy the `Week 0` directory that contains the `SLU000 - Jupyter Notebook` from the `
ds-prep-course` repository to your repository (named `ds-prep-workspace`).  

You can do that either using the command line, or the Operating System's Graphical User Interface.

##### Using the command line

If you have both the `ds-course-prep` and `ds-course-workspace` in a
_projects_ directory you could do it using the command line like this:
```bash
cp -r ~/projects/ds-prep-course/"Week 0" ds-prep-workspace
```

##### Using the Operating System's Graphical User Interface

* On WSL with Ubuntu:
    * first enter the `~/projects/ds-prep-course` directory using the `cd` command, then run `explorer.exe .` (don't forget to include the dot! the dot means "current directory") to open Windows explorer in the current directory:

```bash
cd ~/projects/ds-prep-course
explorer.exe .
```

Windows Explorer should pop up now:

![Sample learning unit](assets/week_0.png "Sample learning unit")

* On Mac:
    * In Finder <img src='assets/finder.png' alt='Finder' width="4%" height="4%"/>, open the "Go" menu, choose the option "Go to folder..."

<img src='assets/go_to_folder.png' alt='Sample learning unit' width="70%"/>

then paste the path to the `ds-prep-course` repository: `~/projects/ds-prep-course`, then click "Go".

<img src='assets/finder_go.png' alt='Sample learning unit' width="90%"/>

### Running a Learning Unit

#### Creating Python Virtual Environment and installing the necessary packages

Bellow are the instructions that are enough to get the setup done and get you up and running :)  
You can also follow [this guide](guides/How_to_set_up_python_virtual_environments.md) for a more in depth set of instructions that accomplish exactly the same thing.

You should always be using a virtual environment to install python packages. We'll use _venv_ to set them up.  

To install and update packages, we'll be using _pip_ is the reference Python package manager.   

If you are using Ubuntu you will need to install a couple of packages first,
this can be done in a terminal by running:
```bash
sudo apt update && sudo apt upgrade && sudo apt install python3-pip python3-venv
```

* Create a virtual environment with the name `prep-venv`
```bash
python3 -m venv ~/.virtualenvs/prep-venv
```
* Activate the environment 

```bash
source ~/.virtualenvs/prep-venv/bin/activate
```

Note: after you activate your virtual environment you should see at the leftmost of your command line the name of your virtual environment surrounded by parenthesis, like this:

```bash
mig@macbook-pro % source ~/.virtualenvs/prep-venv/bin/activate
(prep-venv) mig@macbook-pro %
```
And you're able to make sure your virtual environment is active using the `which` command:

```bash
(prep-venv) mig@macbook-pro % which python
/Users/mig/.virtualenvs/prep-venv/bin/python
```

This means that our virtual environment is active.

*IMPORTANT!!!* make sure that your virtual environment is active before you proceed

* Now you're ready to install packages! Just enter the directory of the `SLU000 - Jupyter Notebook` using the `cd` command, and install the required packages that are enumerated in the `requirements.txt` file

```bash
cd ~/projects/ds-prep-workspace/"Week 0"/"SLU000 - Jupyter Notebook"
pip install -r requirements.txt
```

#### Working on the Learning Unit

All learning units come as a set of Jupyter Notebooks (and some links to
presentations).
Notebooks are documents that can contain text, images and live code that you
can run interactively.

In this section we will launch the Jupyter Notebook application.
The application is accessed through the web browser.

Once you have the application open feel free to explore the sample learning
unit structure.
It will give you a handle on what to expect and what rules the instructors
follow (and the effort they put) when creating a learning unit.

So let's start the Jupyter Notebook app:
* Activate your virtual environment
* Enter the Learning unit directory
* Run the jupyter notebook

```bash
source ~/.virtualenvs/prep-venv/bin/activate
cd ~/projects/ds-prep-workspace/"Week 0"/"SLU000 - Jupyter Notebook"
jupyter notebook
```

1. Activate the environment and run jupyter notebook


##### The Exercise Notebook

Every learning unit contains an exercise notebook with exercises you will
work on.
So let's have a look at the sample Learning Unit. 
1. On the Jupyter Notebook UI in the browser open the exercise notebook
![Open exercise notebook](assets/jupyter_exercise_notebook.png "Open exercise notebook")
1. Follow the instructions provided in the notebook

You'll see cells with the exercises and cells for you to write solutions.

Once you've solved all of the notebook we recommend the following this simple 
checklist to avoid unexpected surprises.
1. Save the notebook (again)
1. Run "Restart & Run All"
![Restart & Run All](assets/jupyter_clear_and_run.png "Restart & Run All")
1. At this point the notebook should have run without any error messages
showing up.
1. When you're done (after saving your work) you can go to the terminal and close it:
<img src='assets/terminal_notebook.png' alt='Sample learning unit' width="70%"/>

#### Commit and Push

Now you have worked on the sample learning unit and you have some uncommitted 
changes.
It's time to commit the changes, which just means adding them to your 
`ds-prep-workspace` repository history, and pushing this history to your 
remote on _GitHub_.

* Using the terminal first make sure you're in the right directory (using the `cd` command), then commit and push the changes
```bash
cd ~/projects/ds-prep-workspace
git add .
git commit -m 'Testing the sample notebook'
git push
```

* Now type your git username, then press <kbd>enter</kbd>
* Then type your git password , then press <kbd>enter</kbd>
* You're all set!

## Learning Unit Workflow

Learning units will be announced in the academy's _#annoucements_ channel.
At this point they are available in the 
[ds-prep-course](https://github.com/LDSSA/ds-prep-couse) 
repository.  
The new Learning Unit is released every Monday, and its 
solutions are then released the next Monday.

The steps you followed during the initial setup are exactly what you are going
to be doing for each new Learning Unit.
Here's a quick recap:
1. Once a new Learning Unit is available at the beginning of each week, pull the changes from the 
[ds-prep-course](https://github.com/LDSSA/ds-prep-couse) repo:
    * enter the `~/projects/ds-prep-course/` using the `cd` command, then use the `git pull` command:
    ```bash
    cd ~/projects/ds-prep-course/
    git pull
    ``` 
    * note that this will also pull the solutions for the Learning Unit of the precious week
1. Copy the Learning Unit to your `ds-prep-course` repo
1. Activate your virtual environment
1. Install the python packages from requirements.txt
1. Work
1. Once all tests pass or once you're happy, commit the changes and push
1. Profit

## Updates to Learning Units

As much as we try and have processes in place to prevent errors and bugs in 
the learning units some make it through to you.
If the problem is not in the exercise notebook you can just pull the new 
version from the ds-prep-course repo and replace the file on your ds-prep-workspace.
The problem is if the correction is in the exercise notebook, you can't just
replace the file because your work is there and you'll lose it!

When a new version of the exercise notebook is released (and announced) you will have to merge the work you've already done into the new version of the
notebook.

At the moment our suggestion to merge the changes is: 
1. Rename the old version
1. Copy the new exercise notebook over
1. Open both and copy paste your solutions to the new notebook

We understand it's not ideal and are working on improving this workflow.

## Help

During the prep-course you will surely run into problems and have doubts about the
material.
Please refer to [this wiki page](https://github.com/LDSSA/wiki/wiki/Data-Science-Prep-Course#how-to-ask-for-help) on how to ask for help!