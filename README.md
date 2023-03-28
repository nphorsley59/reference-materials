# <div align="center">Dev Workflow Reference Materials</div>

# tmux
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


# venv
Tools such as venv support the creation of lightweight “virtual environments”, each with their own independent set of Python packages installed in their site directories. A virtual environment is created on top of an existing Python installation, known as the virtual environment’s “base” Python, and may optionally be isolated from the packages in the base environment, so only those explicitly installed in the virtual environment are available. <br>

The process for creating and activating a virtual environment varies by tool and OS. Virtual environment should be created in the root folder of a project. <br>

NOTE: Online resources may reference "virtualenv"; this is not the recommended tool for Python 3+. <br>

### Unix/macOS
Create a new virtual environment <br>
`python{version} -m venv {venv-name}` <br>

Activate virtual environment <br>
`source {venv-name}/bin/activate` <br>

Deactivate virtual environment <br>
`deactivate` <br>

### Windows
Create a new virtual environment <br>
`{path/to/python} -m venv {venv-name}` <br>

Activate virtual environment <br>
`.\{venv-name}\Scripts\activate` <br>

Deactivate virtual environment <br>
`deactivate` <br>

### Package Management
When used from within an active virtual environment, common installation tools such as pip will install Python packages into a virtual environment without needing to be told to do so explicitly. <br>

Install specific package <br>
`pip install <package-name>` <br>

Install packages from a requirements.txt file <br>
`pip install -r requirements.txt` <br>

### Additional Resources
[https://www.youtube.com/watch?v=28eLP22SMTA&t=444s]

# git
