# dotfiles

These dotfiles are managed through [chezmoi](https://chezmoi.io/), so install it first.

## Prerequisites

-   Git
-   [starship](https://starship.rs/)
-   [Bitwarden CLI](https://github.com/bitwarden/cli)

### Optional

-   [fish](https://fishshell.com) — bash is setup by default

## Setup

```
chezmoi init --apply evoL
```

## Getting tmux-256color to work

Some systems (macOS, Synology DSM) ship with an old version of ncurses. Their terminfo doesn't include `tmux-256color`.

To fix that, install the [terminfo from @nicm](https://gist.github.com/nicm/ea9cf3c93f22e0246ec858122d9abea1):

```sh
curl -o /tmp/tmux-terminfo https://gist.githubusercontent.com/nicm/ea9cf3c93f22e0246ec858122d9abea1/raw/37ae29fc86e88b48dbc8a674478ad3e7a009f357/tmux-256color
tic -x /tmp/tmux-terminfo
```
