# dotfiles-public

Portable configuration shared across my machines.

Nothing machine-specific or secret belongs here.

## Contents

| Path | Notes |
|---|---|
| `config/tmux/tmux.conf` | prefix is `C-Space`; plugins are managed by tpm and not tracked |

## Install

```fish
git clone https://github.com/handsomejack-42/dotfiles-public.git ~/source/dotfiles-public
ln -s ~/source/dotfiles-public/config/tmux ~/.config/tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Then start tmux and press `prefix + I` to install the plugins.

## Terminal keys

The `Ctrl+Tab`, `Ctrl+Shift+Tab` and ``Ctrl+` `` bindings rely on `extended-keys`. Terminals implementing the kitty keyboard protocol send these natively. iTerm2 needs matching Send Escape Sequence entries; the sequences are noted next to each binding.
