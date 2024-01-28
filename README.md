# Chezmoi dotfiles for QI-managed servers

## Prerequisites

* [Oh My Zsh](https://ohmyz.sh) already installed
* [Chezmoi](https://www.chezmoi.io) already installed
* git

## Installation steps (as shell commands)

1. **FreeBSD-specific; ensure chezmoi is there (omit `-r QI` if you’re not at QI):**

    ```sh
    command -v chezmoi > /dev/null 2>&1 || doas pkg install -y -r QI chezmoi
    ```

2. Install powerlevel10k

    ```sh
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
    ```

3. Install and apply these dotfiles

    ```sh
    chezmoi init -a https://github.com/Quinn-Interactive/dotfiles.git
    ```

4. Restart ZSH

    ```sh
    exec zsh
    ```
