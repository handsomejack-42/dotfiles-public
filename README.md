# dotfiles-public

Portable configuration shared across my machines.

Each machine keeps its own dotfiles repository and links to these files from there, so this one is not installed on its own - the consuming repository documents how it does it.

Nothing machine-specific or secret belongs here.

## Contents

| Path | Notes |
|---|---|
| `brew/Brewfile` | cross-platform CLI baseline; formulae only, so it installs on macOS and Linux |
| `config/fish/conf.d/myabbrs.fish` | git abbreviations |
| `config/ompsh/theme.omp.json` | oh-my-posh prompt theme |
| `config/tmux/tmux.conf` | prefix is `C-Space`; plugins are managed by tpm and not tracked |

`brew/Brewfile` is a partial list by design. Never run `brew bundle cleanup` against it, as cleanup uninstalls everything the file does not mention.

## Terminal keys

The `Ctrl+Tab`, `Ctrl+Shift+Tab` and ``Ctrl+` `` bindings in `tmux.conf` rely on `extended-keys`. Terminals implementing the kitty keyboard protocol send these natively. iTerm2 needs matching Send Escape Sequence entries; the sequences are noted next to each binding.
