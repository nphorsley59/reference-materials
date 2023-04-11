# <div align="center">Workflow Reference Materials</div>

## WRITING CODE (PyCharm, Vim/NeoVim)

### PyCharm
PyCharm is a popular Python Integrated Development Environment (IDE) that offers a wide range of features to help with code editing, debugging, testing, and deployment. <br>

**Pros:**
1. Intelligent code completion and error highlighting: PyCharm has excellent code completion and error highlighting features that can help catch errors and speed up coding.
2. Debugging: PyCharm has a powerful debugger that allows you to step through code and identify errors.
3. Built-in tools for testing and version control: PyCharm comes with built-in support for popular testing frameworks like pytest and unittest, as well as version control systems like Git.
4. Customizable and extensible: PyCharm is highly customizable, with support for plugins such as `.ideavim` that can extend its functionality.

**Cons:**
1. Can be resource-intensive: PyCharm can be memory-intensive, and may slow down older or less powerful machines.
2. Can be expensive: PyCharm has a free Community edition, but the Professional edition can be expensive for individual developers or small teams.
3. Large file sizes: PyCharm has large file sizes, which can take some time to download and install.

### Vim/NeoVim
Vim/NeoVim are popular text editors that are known for speed and versatility. With proper configuration, they can be a powerful alternative to an IDE. The primary difference between Vim and NeoVim is which language is used for extension and configuration; Vim relies on Vimscript while NeoVim leverages Lua. <br>

**Pros:**
1. Speed: Vim is fast, responsive, and lightweight, and can handle large files with ease.
2. Powerful editing capabilities: Vim has powerful editing capabilities, including macros, regex search and replace, and a wide range of plugins and extensions that can enhance its functionality.
3. Customizable: Vim is highly customizable, with a wide range of settings and options that can be tailored to the user's preferences.
4. Keyboard-based interface: Vim uses a keyboard-based interface that can be more efficient than a mouse-based interface, once you learn the shortcuts.

**Cons:**
1. Steep learning curve: Vim has a steep learning curve and can take some time to learn and master, especially for developers who are used to graphical text editors.
2. Keyboard-based interface: While the keyboard-based interface can be efficient, it can also be difficult to learn and remember all the shortcuts, especially for developers who are used to a mouse-based interface.
3. Limited GUI capabilities: Vim's graphical user interface (GUI) is relatively basic compared to other text editors, which can make it less appealing to some developers.
4. Limited features out of the box: Vim has fewer features out of the box compared to some other text editors, which can make it less appealing to some developers.

### Additional Resources
[https://intellipaat.com/blog/what-is-pycharm/](https://intellipaat.com/blog/what-is-pycharm/) <br>
[https://neovim.io/](https://neovim.io/)

## TERMINAL MANAGEMENT (tmux)
Tmux is a terminal multiplexer; it allows you to create several "pseudo terminals" from a single terminal. This is very useful for running multiple programs with a single connection, such as when you're remotely connecting to a machine using Secure Shell (SSH). <br>

Tmux also decouples your programs from the main terminal, protecting them from accidentally disconnecting. You can detach tmux from the current terminal and all your programs will continue to run safely in the background. Later, you can reattach tmux to the same or a different terminal. <br>

In addition to its benefits with remote connections, tmux's speed and flexibility make it a fantastic tool to manage multiple terminals on your local machine, similar to a window manager. <br> 

### Setup and Navigation
Create a named session <br>
`tmux new -s {session-name}` <br>

Detach from current session <br>
`ctrl + b, d` <br> 

List available sessions <br>
`tmux ls` <br>

Attach to a named session <br>
`tmux attach -t {session-name}` <br>

Kill a named session <br>
`tmux kill-session -t {session-name}` <br>

### Window and Pane Management
Rename current window <br>
`ctrl + b, ,` <br>

Split window/pane vertically <br>
`ctrl + b, "` <br>

Split window/pane horizontally <br>
`ctrl + b, %` <br>

Navigate between panes <br>
`ctrl + b, {arrow-key}` <br>

Open a new window <br>
`ctrl + b, c` <br>

List available windows <br>
`ctrl + b, w` <br>

### Additional Resources
[https://tmuxcheatsheet.com/](https://tmuxcheatsheet.com/) <br>
[https://gist.github.com/MohamedAlaa/2961058](https://gist.github.com/MohamedAlaa/2961058) <br>
[https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/](https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/) <br>

## VIRTUAL ENVIRONMENTS (venv)
Tools such as `venv` support the creation of lightweight “virtual environments”, each with their own independent set of Python packages installed in their site directories. A virtual environment is created on top of an existing Python installation, known as the virtual environment’s “base” Python, and may optionally be isolated from the packages in the base environment, so only those explicitly installed in the virtual environment are available. <br>

The process for creating and activating a virtual environment varies by tool and OS. Virtual environment should be created in the root folder of a project. <br>

NOTE: Online resources may reference "virtualenv"; this is not the recommended tool for Python 3+. <br>

### Setup and Use
#### Unix/macOS
Create a new virtual environment <br>
`python{version} -m venv {venv-name}` <br>

Activate virtual environment <br>
`source {venv-name}/bin/activate` <br>

Deactivate virtual environment <br>
`deactivate` <br>

#### Windows
Create a new virtual environment <br>
`{path/to/python} -m venv {venv-name}` <br>

Activate virtual environment <br>
`.\{venv-name}\Scripts\activate` <br>

Deactivate virtual environment <br>
`deactivate` <br>

### Package Management
When used from within an active virtual environment, common installation tools such as pip will install Python packages into a virtual environment without needing to be told to do so explicitly. <br>

Install a specific package <br>
`pip install <package-name>` <br>

Install packages from a requirements.txt file <br>
`pip install -r requirements.txt` <br>

### Additional Resources
[https://packaging.python.org/en/latest/guides/tool-recommendations/](https://packaging.python.org/en/latest/guides/tool-recommendations/) <br>
[https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/) <br>
[https://www.youtube.com/watch?v=28eLP22SMTA&t=444s](https://www.youtube.com/watch?v=28eLP22SMTA&t=444s) <br>

## VERSION CONTROL (git)
Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. It allows you to revert selected files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using version control also generally means that if you screw things up or lose files, you can easily recover. With git, you get all this for very little overhead. <br>

Git is the industry standard for version control. <br>

### Best Practices
Establish best practices and team workflows to get the most out of git. <br>

1. Make small, incremental changes
2. Keep commits atomic
3. Develop using branches
4. Write descriptive commit messages
5. Obtain feedback through code review
6. GitFlow or GitHub Flow branching strategy

### Basic Commands
The following are basic commands that are core to the git workflow. If you understand the big picture of how git works and are careful, you will rarely need other commands. <br>

Clone a remote git repository <br>
`git clone {repository-address}` <br>

Change branch <br>
`git checkout {branch-name}` <br>

Create a new branch <br>
`git checkout -b {new-branch-name}` <br>

Check status of current branch <br>
`git status` <br>

Stage change <br>
`git add {path/to/file}` <br>

Commit change <br>
`git commit -m {commit-message}` <br>

Push local commits to remote <br>
`git push` <br>

Pull remote commits to local <br>
`git pull` <br>

Stash local changes <br>
`git stash` <br>

Unstash stashed changes <br>
`git stash pop` <br>

Merge branches <br>
`git merge {branch-name}`

### Additional Resources
[https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) <br>
[https://ohshitgit.com/](https://ohshitgit.com/) <br>
