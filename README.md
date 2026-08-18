# dotfiles-public

Portable configuration shared across my machines.

Nothing machine-specific or secret belongs here.

## Contents

| Path | Notes |
|---|---|
| `brew/Brewfile` | cross-platform CLI baseline; formulae only, installs on macOS and Linux |
| `config/tmux/tmux.conf` | prefix is `C-Space`; plugins are managed by tpm and not tracked |
| `config/ompsh/theme.omp.json` | oh-my-posh prompt theme |
| `config/fish/conf.d/myabbrs.fish` | git abbreviations |

## Install

```fish
git clone https://github.com/handsomejack-42/dotfiles-public.git ~/source/dotfiles-public
cd ~/source/dotfiles-public

brew bundle install --file brew/Brewfile

ln -s ~/source/dotfiles-public/config/tmux ~/.config/tmux
ln -s ~/source/dotfiles-public/config/ompsh ~/.config/ompsh
ln -s ~/source/dotfiles-public/config/fish/conf.d/myabbrs.fish ~/.config/fish/conf.d/myabbrs.fish
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Then start tmux and press `prefix + I` to install the plugins.

`brew/Brewfile` is deliberately a partial list, so never run `brew bundle cleanup` against it - cleanup uninstalls everything the file does not mention.

## Terminal keys

The `Ctrl+Tab`, `Ctrl+Shift+Tab` and ``Ctrl+` `` bindings rely on `extended-keys`. Terminals implementing the kitty keyboard protocol send these natively. iTerm2 needs matching Send Escape Sequence entries; the sequences are noted next to each binding.
