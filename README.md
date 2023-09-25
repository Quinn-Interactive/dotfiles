# Chezmoi dotfiles for QI-managed servers

Installation steps (as shell commands):

1. `command -v chezmoi > /dev/null 2>&1 || doas pkg install -yr QI chezmoi`
1. `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
1. `chezmoi init https://github.com/Quinn-Interactive/dotfiles.git`
1. `chezmoi apply`
1. `omz reload`
