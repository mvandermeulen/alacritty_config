# Alacritty Config

## Overview

Custom [Alacritty](https://alacritty.org) configuration for use on MacOS. Includes custo keybindings used
to integrate with [Tmux](https://github.com/tmux/tmux).

### Related

- [My Tmux Configuration](https://github.com/mvandermeulen/local-tmux)

## Install

1. Install Alacritty with `brew install alacritty`
2. Link configuration
    2.1. Exact file: `$HOME/.config/alacritty/alacritty.toml` -> `./config/alacritty.toml` OR
    2.2. Directory: `$HOME/.config/alacritty` -> `./config`

```
#git clone git@github.com:mvandermeulen/alacritty_config.git
git clone git@github.com:mvandermeulen/dots.git
cd dots
export ALACRITTY_CONFIG_DIR="$HOME/.config/alacritty"
if [[ -d "$ALACRITTY_CONFIG_DIR" ]]; then
    TODAYS_DATE=$(date +"%Y%m%d"); ALACRITTY_CONFIG_BACKUP_PATH="${ALACRITTY_CONFIG_DIR}_${TODAYS_DATE}";
    mv "$ALACRITTY_CONFIG_DIR" "${ALACRITTY_CONFIG_BACKUP_PATH}"
    echo "Moved existing Alacritty configuration to ${ALACRITTY_CONFIG_BACKUP_PATH}"
fi
ln -s "$(pwd)/alacritty/config" $ALACRITTY_CONFIG_DIR
```


