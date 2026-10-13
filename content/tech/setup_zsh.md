---
title: "How to setup zsh in Fedora"
date: 2026-09-22
---

# Install zsh

install zsh through package manager

```bash
sudo dnf install zsh
```

Then, change the default shell script to zsh

```bash
chsh -s $(which zsh)
```

# Option 1: manage extension through oh my zsh

Github repo of oh my zsh is [here](https://github.com/ohmyzsh/ohmyzsh).

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

install a nerd font, such as MesloLGS, for powerlevel10k display.

continue installing the extensions/plugins for zsh

```bash
# 1. Download Powerlevel10k Theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# 2. Download Autocomplete (Autosuggestions)
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# 3. Download Syntax Highlighter
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

write config into `~/.zshrc`:

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```

ensure `zsh-syntax-highlighting` should always be listed **last**

save the file and reload your shell configuration:

```bash
source ~/.zshrc
```

The powerlevel10k configuration will automatically start at next terminal startup.

# Option 2: manage on my own

Without a layer of oh my zsh to manage every plugin and component of zsh, the startup speed will be a lot faster and the burden to the system is smaller. I personally really like this.

```bash
# Create the directory and clone Powerlevel10k, zsh-autosuggestions, and zsh-syntax-highlighting into ~/.zsh
mkdir -p ~/.zsh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.zsh/powerlevel10k
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting
```

edit `~/.zshrc`:

```bash
# Enable Powerlevel10k Instant Prompt and source themes/plugins
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

source ~/.zsh/powerlevel10k/powerlevel10k.zsh-theme
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

remember to setup a nerd font in the terminal preference. I use FiraCode Nerd Font.


