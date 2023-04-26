## configs:

### tmux tpm

https://github.com/tmux-plugins/tpm

1. git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
2. Put this at the bottom of ~/.tmux.conf ($XDG_CONFIG_HOME/tmux/tmux.conf works too):
  ```
  # List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'github_username/plugin_name#branch'
# set -g @plugin 'git@github.com:user/plugin'
# set -g @plugin 'git@bitbucket.com:user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
  ```
3. Reload TMUX environment so TPM is sourced:
```
# type this in terminal if tmux is already running
tmux source ~/.tmux.conf
```
That's it!

## Installing plugins

  1. Add new plugin to ~/.tmux.conf with set -g @plugin '...'
  2. Press prefix + I (capital i, as in Install) to fetch the plugin.
  
You're good to go! The plugin was cloned to ~/.tmux/plugins/ dir and sourced.

## Uninstalling plugins
  
  1. Remove (or comment out) plugin from the list.
  2. Press prefix + alt + u (lowercase u as in uninstall) to remove the plugin.
  
  All the plugins are installed to ~/.tmux/plugins/ so alternatively you can find plugin directory there and remove it.
  
  ```prefix + I``` Installs new plugins from GitHub or any other git repository
