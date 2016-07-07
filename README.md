govim
---
Minor modifications to mbrt/golang-vim-dev to work with tmux and all powerline characters.

mac
---
Process I followed.

 * Install [iTerm2](https://www.iterm2.com/) if you haven't already.
 * Install a [powerline compatable font](https://github.com/powerline/fonts) through Mac's built in Font Book. I'm using Droid Sans Mono for Powerline.
 * Configure iTerm to use the powerline fonts. In Preferences > Profiles > Text and select a powerline font you installed.
 * Use `export TERM=screen-256color` inside the container to remove two tone backgrounds from vim inside tmux. More details and options [here](http://superuser.com/questions/399296/256-color-support-for-vim-background-in-tmux).
 * Add `let g:airline_powerline_fonts = 1` to .vimrc to populate the airline symbols dictionary. [Reference](https://github.com/bling/vim-airline/wiki/FAQ)
 * To fix the odd "hanging" characters I used @devlinzed solution. [Reference](https://github.com/bling/vim-airline/issues/17#issuecomment-23868747)

> If you bork your default profile and need to reset iTerm2 you can close out of the app and run `defaults delete com.googlecode.iterm2` from mac default terminal to reset. [Reference](http://apple.stackexchange.com/questions/164821/restoring-iterm2-to-default-values)
