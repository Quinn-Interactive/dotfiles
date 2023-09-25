# Chezmoi dotfiles for QI-managed servers

## Prerequisites

* [Oh My Zsh](https://ohmyz.sh) already installed
* [Chezmoi](https://www.chezmoi.io) already installed
* git

## Installation steps (as shell commands)

1. **FreeBSD-specific; ensure chezmoi is there (omit `-r QI` if you’re not at QI):**
    `command -v chezmoi > /dev/null 2>&1 || doas pkg install -y -r QI chezmoi`
1. `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
1. `chezmoi init https://github.com/Quinn-Interactive/dotfiles.git`
1. `chezmoi apply`
1. `omz reload`
