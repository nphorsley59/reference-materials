# reference-materials

# tmux
Tmux is a terminal multiplexer; it allows you to create several "pseudo terminals" from a single terminal. This is very useful for running multiple programs with a single connection, such as when you're remotely connecting to a machine using Secure Shell (SSH). <br>

Tmux also decouples your programs from the main terminal, protecting them from accidentally disconnecting. You can detach tmux from the current terminal and all your programs will continue to run safely in the background. Later, you can reattach tmux to the same or a different terminal. <br>

In addition to its benefits with remote connections, tmux's speed and flexibility make it a fantastic tool to manage multiple terminals on your local machine, similar to a window manager. <br> 

### Setup and Navigation
1. Create a named session <br>
`tmux new -s {session-name}` <br>

2. Detach from current session <br>
`ctrl + b, d` <br> 

3. List available sessions <br>
`tmux ls` <br>

4. Attach to a named session <br>
`tmux attach -t {session-name}` <br>

5. Kill a named session <br>
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
