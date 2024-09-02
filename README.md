# Preparatory Assignment: Hello world.

The goal of this exercise is to set up your computing environment and practice the workflow we will be using in our pre-course programming material. You will set up a Unix operating system (if you'd like), a distributed version control system for files `git`, `Python` with `pyenv` — version control tool for `Python`, a code editor, and `pytest`, as well as practice using git in the Github Classroom workflow.

### Instructions

1. I would suggest you to setup a Unix operating system. It is often considered to be a first choice for data/computer science professionals, as it provides flexibility in terms of package and permission management. 

    Let's first discuss what to do if you want to try a Unix-type OS. In effect, it's either Mac or Linux. If you already use a Mac, it's fine to just stick with it. If you want to install Linux, I recommend [Ubuntu](https://ubuntu.com/) or [Manjaro](https://manjaro.org/). Ubuntu is a bit more popular and the internet is full of guides, which is nice for first-time Linux users, but Manjaro has a great package manager. Any Linux distribution will do, so feel free to read a bit and choose one that you think you will like. There exists an option to install Linux in a separate partition alongside your current Windows OS, but I encourage you to research on the matter on your own if this is the path you are willing to take.

    If you decide to continue using Windows, you may still be able to use a Unix-like command line interface. I strictly recommend you to read more about a Windows Subsystem for Linux (WSL), e.g. check out [this page](https://learn.microsoft.com/en-us/windows/wsl/install). There you can also find some information on how to change the default Linux distribution that the subsystem emulates if needed. This tool should open up a little bit the potential of your machine in terms of performing OS-related operations.

2. Learn to use the terminal (also called console) on your system. In short, it allows you to communicate with your OS to perform some tasks which can vary from basic, like opening up an app, creating/deleting/copying/operating a file/directory, to more complex, such as creating a pipeline which would download data from some server in the internet, save it in a prepared spot in you computer, and then porocess it and yield some output.

    Both MacOS and any Linux distribution will come with a terminal, in Mac and Ubuntu (Gnome) this is called "Terminal", in KDE Linux distros it is "Konsole". These applications are _terminal emulators_ and provide a _command line interface_ to your operating system via a _shell_ program (usually either _bash_ or _zsh_). Don't worry about all those terms, that sentence is there so that you can start to become familiar with them and recognize them.

    * [This is a great guide to using the terminal](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview). It's created by Ubuntu, but works perfectly for any Linux user and the first few sections should work for Mac as well.

3. Get to know your package manager. For Linux, you will have a default package manager (apt, pacman, yum, etc.). Read a bit about package management on your operating system. For MacOS, I recommend using [Homebrew](https://brew.sh/). Package managers will let you install/manage applications for your system and allow you to do it all from the terminal by the means of some handy and not so long commands, which should simplify your life as a future developer, analyst, or — in broader terms — a data scientist.

4. Using your package manager, install `git` on your system if you don't already have it. To check if you have it, run `git --version` from the terminal. It is a version control system, which allows to create repositories, i.e. collections of files and directories, modify them, and easily operate and follow the workflow. For example, using this tool one can create checkpoints throughout the development of the repository, and revert the changes in the future if needed. In addition, it allows to create work on several files or locations in a single file at the same time using two or more separate "branches" without damaging the previous progress. These features shine brighter in the presense of web-interfaces like [GitHub](https://github.com) which allows to deploy repositories online, share them, and collaborate with other developers.

    `Git`'s efficiency comes from the way it keeps the record of the versions of a repository. On a high level, at each checkpoint it stores only the changes that occured in comparison the the previous state of a repo, avoiding keeping each occuring version entirely. 

    You can check out the [official `git` homepage](https://git-scm.com) to read more about `git` and find an official documentation. Feel free to explore it! Note: the only features you will need for now are `clone`, `commit`, and `push`. You can also find the latest available version of `git` on this page. If you have an older version, you can use your package manager to install the latest. It's a good practice to keep up with the latest versions of your tools.

    Here are a couple of extra guides for learning what git is and how to use it:

    * [Hello World using just Github](https://guides.github.com/activities/hello-world/)
    * [Introduction to git on the command line](https://towardsdatascience.com/getting-started-with-git-and-github-6fcd0f2d4ac6)

5. When you use `git` together with `GitHub`, you will need to connect the two, i.e. to setup your `GitHub` credentials in your local `git`. I highly recommend you to use `GitHub CLI` (command line interface). See [this page](https://cli.github.com) to find an installation guide and read more. When you install `GitHub CLI`, you should be able to run `gh auth login` in your terminal to open authenticate via `GitHub` and cache your credentials in `git`. Read more [here](https://cli.github.com/manual/gh_auth_login). By doing all that, you facilitate drastically the deployment of your local repos in GitHub and any work with external repos. Moreover, you ensure that your GitHub account will be directly associated with the repos you will be working on in the future.

6. "Clone" this repository. Cloning and repositories are both concepts from git, which you can read about in the previous guides. Basically, it means "copy files from a remote server to my local computer". With cloning, in addition to the files themselves, you get the "version history" as well.

7. Right now, what you're reading is actually the `README.md` file of this repository. You're probably reading it online, but now that you've cloned the repository to your local computer, you should have this file there too! Go ahead and try and read it. It's a "markdown" file. You can open it in any program that reads plain text files or by using `cat` from the command line.

8. Now we shall setup`Python3`.

    First, install `python-tk`. For Linux Ubuntu distribution you can do it running the following command in your terminal: `sudo apt-get python3-tk`. Maybe you will need to change the name from `python3-tk` to `python-tk`. For Mac, install it via Homebrew by running the following command in your terminal: `brew install python-tk`.

    Now, you are going to install `pyenv` which manages `Python` environments and versions. It is a good practice to create separate environments for different projects. An environment, in effect, is comprised of a version of `Python` and installed `Python` packages which provide useful functions and data structures to indegrate with your program. 

    See the installation guide here [here](https://github.com/pyenv/pyenv#installation). Do not forget to also setup your shell environment to use pyenv, see the detailed guide [here](https://github.com/pyenv/pyenv#set-up-your-shell-environment-for-pyenv).

    Now, you can check which `Python` versions are installed by running in your terminal: `pyenv versions`. Then, you can install a `Python` version like this: `pyenv install 3.11`. Then, to make this version global on your computer, run: `pyenv global 3.11`. You can also install other version than the one used in the example. See which versions are available and considered "stable" [here](https://devguide.python.org/versions/). 

    Now, you should have `python` and `pip` symbolic links, associated to this python version, ready to call them in a terminal.

    * _Background:_ there are two "major" `Python` versions: "2" and "3". In general, you should do all your programming in `Python3` now, as `Python2` is deprecated. However, there are some old programs that still use `Python2` and your operating system might use one of these old programs and might have `Python2` installed already. If that is the case, don't overwrite the `Python2` installation on your computer, you can have both and use `Python3` for your programming.

9. Install an editor or integrated development environment (IDE) that you can use to write `Python` code. Here are a few text editor options:

    * I recommend installing [VSCode](https://code.visualstudio.com/), which is supported by Microsoft and an active open source community. It has a huge library of plugins, and supports numerous programming languages.
    * There are also solutions from JetBrains. The `Python` IDE they have is called [PyCharm](https://www.jetbrains.com/pycharm/).
    * [Atom](https://atom.io/) is a really nice open source project that's also very easy to use and customize. It was created by the folks at Github, which was recently bought by Microsoft.
    * [Vim](https://www.vim.org) is a very powerful text editor. It can be configured any way you want, but has a very steep learning curve. You can also check out [Neovim](https://neovim.io) which is a fork of Vim which also allows to use a powerful programming language called Lua for file management and more.
    * [Emacs](https://www.gnu.org/software/emacs/) can be considered as an alternative for Vim. It also has a steep learning curve, but the hard work pays out by flexibility you gain in the end. [Doom-emacs](https://github.com/hlissner/doom-emacs) is a great batteries-included version that is easy to get started with.

    You should then install the appropriate `Python` plugins/extensions for your IDE. Try to open this folder in your editor, where you should be able to read this file as well as the `Python` files `exercises.py` and `test_exercises.py`.

10. We also want to be able to open, run, and modify Python notebooks. 

    `Python` scripts have an extension `.py`, as the exercises file in the current repo. These scripts are run by `Python` interpreter line by line (that's a very much simplified explanation), and typically do not allow to write new code or modify existing one on the go. However, there also `Python` notebooks that have an extension `.ipynb` which allow to do all that, and are usually used by data analysts and other professionals to work on projects which involve exploration of some data and presenting the results by means of statistics and/or graphics. 

    First, install Jupyter Notebook by running `pip install notebook`. You should be able to run Jupyter notebook by running `jupyter notebook` command in your terminal; it will start a local server on your machine which will be used for running `Python` notebooks and scripts.

    If you chose VSCode as your primary IDE, then you should be also able to install an extention through it to be able to run `Python` notebooks directly there. Explore this option on your own.

11. Install the `Python` package `pytest` on your machine. You can do it globally by running `pip install pytest` in your terminal. If you know about virtual environments (or want to learn on your own), you can install `pytest` just in a virtual environment you create for each of the assignments. Otherwise, it is also fine to install it into the your global `Python` environment.

12. You should now be able to run the command: `pytest` in your terminal, inside this folder. The `pytest` package has installed this command globally and it is available anywhere from your terminal, however, it's behavior will change based on what folder you are in (in the terminal). When run from inside this folder, the `pytest` program will run all the "tests" in this exercise.

    Tests are used a lot in programming to ensure that our code does what we want it to do. We will use tests in all our "learning Python" assignments. The tests will "fail" until you have written code that performs the assignment correctly, at which point it will "pass".

13. Open the `exercises.py` file and complete the assignment. Run `pytest` again to see if you completed the assignment correctly. If the test passes, you're done!

14. To "turn in" the assignment you will need to _commit_ your changes and _push_ them to the Github repository you've cloned.

*Credits: Jordi Llorens, Maxim Fedotov.*
