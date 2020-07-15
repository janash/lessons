---
title: Setup
---

# Setup
Participation in the MSSE Bootcamp will require use of your own personal computer or laptop and installation of some software.

Please follow the instructions given here to make sure you have the necessary software installed. We will be using Python and the conda package manager from Anaconda. We will be installing both using `miniconda`. Another option would be to install Anaconda. If you have Anaconda installed already, you should be fine, it will work for all of our excercises.

Both miniconda and Anaconda include a Python distribution and the `conda` package manager. However, Anaconda includes several python libraries bundled alongside as well. We choose miniconda because it takes up less space and we can add the packages we need as we need them. If you would prefer to install Anaconda, you are free to do that.

Again, please read this page in its entirety. After you have installed miniconda, there are instructions for creating an environment using conda. 

Installation varies by operating system (OS).

## Windows
If your computer uses the Windows operating system, we strongly recommend installing Windows Subsystem for Linux (WSL). Follow the installation instructions at [this link](https://docs.microsoft.com/en-us/windows/wsl/install-win10). See theIf you don’t have a preference on Linux distribution, we recommend installing Ubuntu 20.04. 

Once WSL is installed, open your ‘Start’ menu and choose ‘Ubuntu’. This should open a terminal window. The first time you have opened Ubuntu, you will see a message which says “Installing, this may take a few minutes…”. After the installation is done, you will have to create a username and password. After these are created, you should be able to use the terminal.

For the WSL, you have to install miniconda from the terminal in your Linux operating system. Note that if you if you are using the WSL, your Linux OS is completely separated from your Windows operating system. This means that software installed on one operating system is not available in the other.

You are now using a Linux OS under Windows. For the rest of the install instructions, see the Linux section, below.

## Linux

If you are on Linux (not WSL), you can download and run the installer at this [link](https://docs.conda.io/en/latest/miniconda.html). If you are using the WSL or would like to use the command line to install, see the instructions below.

To install miniconda from the command line, execute the following lines in your terminal:  

~~~
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
~~~
{: .language-bash}

After installation, close and reopen your terminal window. If you do not see (base) before your username on the command line, type

~~~
conda init
~~~
{: .language-bash}

### Compilers
After installing miniconda, you will need to install compilers for the C++ section of the course. Use this command to install compilers
~~~
sudo apt install build-essential
~~~
{: .language-bash}

## Mac OS and Linux

You can download and run the installer at this [link](https://docs.conda.io/en/latest/miniconda.html). If you are using the WSL or would like to use the command line to install, see the instructions below.

To install miniconda from the command line, execute the following lines in your terminal:  

~~~
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh
~~~
{: .language-bash}

After installation, close and reopen your terminal window. If you do not see (base) before your username on the command line, type

~~~
conda init
~~~
{: .language-bash}

### Compilers
MacOS users should also [install XCode](https://developer.apple.com/xcode/). An easy way to install XCode is through the [Mac App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12).


# Creating a MSSE Bootcamp conda environment
Everyone should complete and read this section after installing miniconda.

To make a great deal of compilation and installation simpler we will create a conda environment. Environments isolate software from this project from the rest of the dependencies on your laptop.

After installing miniconda, type the following command into your terminal. This creates an environment called “msse-python” which runs Python 3.7.


~~~
conda create -n msse-python python=3.7
~~~
{: .language-bash}

After creating the environment, activate it using the command

~~~
conda activate msse-python
~~~
{: .language-bash}

Next, install the Python libraries jupyter and matplotlib

~~~
conda install matplotlib
conda install jupyter
~~~
{: .language-bash}

You now have a new environment `msse-python` created which has the Python Standard Library, matplotlib, and jupyter installed. This is the environment we will be using for our initial coding projects.

To deactivate the environment, use

~~~
conda deactivate
~~~
{: .language-bash}


## Installing and configuring git <a name="git_configuration"></a>

### Installation
We will be using the `git` software for version control during this course. This portion walks you through installing and configuring `git`.

If you do not have the environment activated, activate it first:

~~~
conda activate msse-python
~~~
{: .language-bash}

Next, install `git`

~~~
conda install git
~~~
{: .language-bash}

### Configuring Git

The first time you use Git on a particular computer, you need to configure some things.

First, you should set your identity.
One of the most important things that version control like Git does is to keep track of who changes what.
This helps repository maintainers coordinate the efforts of all the people who contribute to the project.
Most importantly, it makes it easier to figure out who to blame when something goes wrong.
You can provide git your name and contact information with the following commands:

~~~
git config --global user.name "<Firstname> <Lastname>"
git config --global user.email "<email address>"
~~~

Next, you might want to change the Git text editor.
As we will see later, certain Git commands will open text files.
When this happens, Git will use your environment's default text editor, which might not be the editor you are most comfortable using.
Using configuration commands, you can tell Git to use your favorite editor.

Everyone can use Vim as a text editor, but you can set it to your preference. **If you are using the WSL, use Vim as your text editor**:

~~~
$ git config --global core.editor "vim"
~~~

A more complete list of possible editors is available [here](http://swcarpentry.github.io/git-novice/02-setup/index.html).

You can check the configuration commands that you have set using:

~~~
git config --list
~~~

## Text Editor/IDE
Everyone should have a text editor they can use to edit Python. If you do not have a preference for text editors, we recommend [Visual Studio Code](https://code.visualstudio.com/). If you are using WSL, see [these instructions](https://code.visualstudio.com/docs/remote/wsl) for installing Visual Studio Code for use with WSL





