# Customized Tmux Configuration

This Tmux configuration is tailored to enhance your terminal experience. Below are some key features and explanations for each section:

## 1. Terminal Overrides


```bash
set-option -sa terminal-overrides ",xterm*Tc"
```
This line sets terminal overrides, ensuring compatibility with xterm.

## 2. Prefix Remapping
```bash
unbind C-b
set-option -g prefix C-a
bind-key C-a send-prefix
```
Remaps the default prefix from C-b to C-a for convenience.

## 3. Pane Splitting
```bash
bind | split-window -h -c "#{pane_current_path}"
bind - split-window -v -c "#{pane_current_path}"
```
Enables horizontal splitting with | and vertical splitting with -.

## 4. Reload Configuration

```bash
bind r source-file ~/.config/tmux/tmux.conf
```
Binds r to reload the Tmux configuration, facilitating quick updates.

## 5. Mouse Control and Status Bar

```bash
set -g mouse on
set-option -g status-position top
```
Enables mouse control for clickable windows and panes. Positions the status bar at the top.

## 6. Window and Pane Indexing
```bash
set -g base-index 1
set -g pane-base-index 1
set-window-option -g pane-base-index 1
set-option -g renumber-windows on
```
Starts window and pane indexing at 1 instead of 0, providing a more intuitive numbering system.

## 7. Escape Time
```bash
set -sg escape-time 50
```
Adjusts the escape time, enhancing responsiveness.

## 8. Plugin Configuration
```bash
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'christoomey/vim-tmux-navigator'
set -g @plugin 'catppuccin/tmux'
```
Configures Tmux plugins for additional functionality. You can manage these plugins using Tmux Plugin Manager (TPM).

## 9. TPM Initialization
```bash
run '~/.tmux/plugins/tpm/tpm'
```
Initiates TPM to ensure proper functioning of the configured plugins.

Feel free to customize these settings to suit your preferences and workflow. Enjoy your improved Tmux experience!
