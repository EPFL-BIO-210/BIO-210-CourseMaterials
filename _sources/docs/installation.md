# Visual Studio Code, Git and Anaconda

## Visual Studio Code

### Introduction

An integrated development environment (IDE) is a software application that augments the computer programmer abilities by offering a source code editor, build automation tools, a debugger (and other features). From the most popular IDE for Python programmers (e.g. Visual Studio Code, PyCharm, Atom, Spyder, Sublime or IDLE), we selected Visual Studio Code as it is open-source, highly customizable and it provides a lot of useful resources such as extensions, code completion and git integration. Visual Studio Code is a lightweight but powerful source code editor which runs on desktop and is available for Windows, macOS and Linux. It comes with a rich ecosystem of extensions and built-in support for many languages and runtimes (such as C++, C#, Java, Python, PHP, Go, .NET).

### Configuration

Start your journey using Visual Studio Code with a set of introductory videos, available at the official [VS Code website](https://code.visualstudio.com/docs/getstarted/introvideos). These videos are designed to give you an overview of VS Code's various features and quickly get you familiar with them. In the scope of our course, familiarize yourself with [the beginner tutorial](https://code.visualstudio.com/docs/introvideos/basics) and [the code editing guide](https://https://code.visualstudio.com/docs/introvideos/codeediting).

You can also configure your VS Code into a great, lightweight Python IDE by using the official Python extension. Follow [this tutorial](https://code.visualstudio.com/docs/python/python-tutorial) to get started with Python in VS Code.

The Python extension supports debugging of several types of Python applications. Follow [this tutorial](https://code.visualstudio.com/docs/python/debugging) for a short walkthrough of Python-specific debugging configurations, including the necessary steps for specific app types and remote debugging. For general debugging features such as inspecting variables, setting breakpoints, and other activities that are not language-dependent, please review [VS Code debugging](https://code.visualstudio.com/docs/editor/debugging).

## Git

For your projects, you will use Git which is a free and open source distributed version control system. Let's see for now how to install it and use it to clone the BIO-210 repository as you previously did on NOTO.

### Installation

##### Windows

- Go to [Git for Windows](https://gitforwindows.org/)
- Download the latest version and start the installer
- Follow the Git Setup wizard
- Open the windows command prompt (or Git Bash)
- Type: `git --version`   (to verify git is installed)

##### Mac

- Open the command prompt "terminal".
- Type: `git`. If it is not installed, a pop-up window will appear asking you to install XCode, which includes git. Simply click on "Install" and follow the instructions. If `git` is already installed, you will see the git help message instead.
- Finally, type: `git --version`  (to verify git is installed)

##### Linux

Git is already pre-installed on Linux, so you do not need to install it.

### Clone the BIO-210 repository

Go in the folder in which you want to clone the class repository:

`cd [insert_your_folder]`

Clone the class repository:

`git clone https://github.com/EPFL-BIO-210/BIO-210-CourseMaterials.git`


## Anaconda

In previous lectures, you have seen the functions related to different Python packages (in particular Numpy needs to be installed). When developing a project, you might need to install a specific set of packages. Usually, you might have different projects with different requirements, and you do not want to have a conflict between packages. Therefore, a possible solution consists in using Anaconda and virtual environments.

Anaconda is a distribution of Python used for package management and deployment. Conda analyzes the current environment (including everything currently installed and related version limitations) and works out how to install a compatible set of dependencies. When Anaconda is being installed, it automatically comes with Python, 250 packages and the virtual environment manager.

### Installation

##### Windows

- Follow the instructions of the following link: [Anaconda for Windows](https://docs.anaconda.com/anaconda/install/windows/)
- Open anaconda prompt
- Type: `python --version`  (to verify python is installed)

##### Mac

- Follow the instructions of the following link: [Anaconda for Mac](https://docs.anaconda.com/anaconda/install/mac-os/)
- Open terminal
- Type: `python --version`   (to verify python is installed)

##### Linux

- Follow the instructions of the following link: [Anaconda for Linux](https://docs.anaconda.com/anaconda/install/linux/)
- Open terminal
- Type: `python --version`  (to verify python is installed)

### Tutorial

Conda can be used to create environments to isolate your projects. This means that each project can have its own dependencies, regardless of what dependencies every other project has.

Create a virtual environment giving it a name 'env_name' (you can choose the name you prefer, best to be related to the project))):

`conda create -n env_name`

If you want to use a specific version of Python, you can specify it as:

`conda create -n env_name python=3.8`

Once you have generated an environment, you can access it to manage your packages or run your python applications:

`conda activate env_name`

You should observe that on the left of the terminal (base) changed in (env_name). This means that you are in the virtual environment now and ready to manage your python environment for you specific project!

For example, let’s install jupyter lab in our virtual environment:

`conda install -c conda-forge jupyterlab`

Note that conda might not have all the packages you need. In this case, you can use pip to install the missing packages (for a comparison between conda and pip, you can have a look [here](https://pythonspeed.com/articles/conda-vs-pip/)), e.g.:

`pip install numpy`

Remaining inside the generated virtual environment, we can navigate to the class repository.

`cd [path-to-BIO-210-COURSE-MATERIAL]`

Now, we can access the notebooks using jupyter lab:

`jupyter lab`

Once, you have finished working on your project, you can exit your virtual environment with the following command:

`conda deactivate env_name`

## Additional materials (not required)

Almost every part of VS Code can be customized and enhanced through the Extension API. Here we provide some of the most useful additional extensions:

* [SSH extension](https://code.visualstudio.com/docs/remote/ssh) - allows to open a remote folder on any remote machine, virtual machine, or container with a running SSH server;

* [Docker container extension](https://code.visualstudio.com/docs/remote/containers) - allows to open any folder inside (or mounted into) a container and take advantage of VS Code's features.
