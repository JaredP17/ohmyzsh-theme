# Oh My Zsh Theme: "custom"

## Prerequisites

* A macOS operating system. Other Unix like systems may work with tweaking, but this has only been setup to work on macOS as of now.
* [Zsh](https://www.zsh.org) should be installed (v4.3.9 or more recent). If not pre-installed (run `zsh --version` to confirm), check the following instructions here: [Installing ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
* Oh My Zsh should be installed. To learn more, visit [ohmyz.sh](https://ohmyz.sh)
* Installing [Nerd Fonts](https://www.nerdfonts.com/) is required for my theme to render properly. 

_Note: many other themes aside from my own require installing the [Powerline Fonts](https://github.com/powerline/fonts) in order to render properly. (e.g. "agnoster")._

## Basic Installation
1. Clone/download this repository to your computer.
2. Move the `custom.zsh-theme` file into the `~/.oh-my-zsh/themes` directory.
3. See below about enabling theme.


### Enabling Theme

_"Robby's theme is the default one. It's not the fanciest one. It's not the simplest one. It's just the right one (for him)."_ - Oh My Zsh

If you'd like to use my theme, you will need to edit the `~/.zshrc` file. You'll see an environment variable (all caps) in there that looks like:

```shell
ZSH_THEME="robbyrussell"
```

To use my theme, simply change the value to match the name of the theme. For example:

```shell
ZSH_THEME="custom"
```

### Conditional Theming
My theme looks favorably in both the Apple Terminal and Visual Studio Code.  However, it isn't so favorable in iTerm2. To combat this issue, I wrote a script within `~/.zshrc` to use the _"agnoster"_ theme with iTerm2 instead. For example:

```shell
# If running iTerm2
if [ "$TERM_PROGRAM" = "iTerm.app" ]; then
    ZSH_THEME="agnoster"

# If running Apple Terminal or Visual Studio Code
elif [ "$TERM_PROGRAM" = "Apple_Terminal" ] || [ "$TERM_PROGRAM" = "vscode" ]; then 
    ZSH_THEME="custom"

# Default zsh theme
else
    ZSH_THEME="robbyrussell" 
fi
```

#
## My CLI Preferences

### Apple Terminal:
* Homebrew color profile
* Font: SauceCodePro Nerd Font
* Oh My Zsh Theme: custom

### iTerm2:
* Solarized Dark color profile
* Font: Hack
* Oh My Zsh Theme: agnoster

### Visual Studio Code:
* Default Dark+ color profile
* Font: SauceCodePro Nerd Font
* Oh My Zsh Theme: custom

## Previews

### Home directory, after running neofetch command
_Note: neofetch is a homebrew package._

_Apple Terminal_
![Apple Terminal](./images/term.png)

_iTerm2_ - Uses the _"anoster"_ theme with my conditional script
![iTerm2](./images/iterm.png)

_Visual Studio Code_
![Visual Studio](./images/vscode.png)

### Within a Git repository

Clean Working Tree
![Clean Working Tree](./images/term-git-clean.png)

Unclean Working Tree
![Unclean Working Tree](./images/term-git-dirty.png)
#

## Contributors

Open to accepting new contributors.

## Licenses
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Credits
* Oh My Zsh theming documentation.
* Inspiration based on "robbyrussell" and "gnzh" themes.