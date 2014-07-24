dotfiles
=======================

This repo contains learnings and tools I've gathered from becoming a full fledged Front-End Developer

### Settings up my development environment
1. Install HomeBrew first
2. Install Google Chrome and iTerm2
3. Use Terminal to configure iTerm2 to my preferred settings

```
killall cfprefsd     # This will get rid of cached settings
rm  ~/Library/Preferences/com.googlecode.iterm2.plist
ln -s ~/dotfiles/com.googlecode.iterm2.plist ~/Library/Preferences/com.googlecode.iterm2.plist
```

4. Now, Install oh-my-zsh
5. Remove pygmalion theme
6. Copy and paste my pygmalion theme 
7. vim up .zshrc file and change zsh theme = russell to pygmalion

### Setting up my VIM theme and configs
1. Copy ```.vim``` and ```.vim-rc``` unto root directory
```
cd ~/dotfiles/
cp -R .vim .vim-rc ~/
```
2. Now, type ```vim ``` on iTerm
3. and type ```:E``` for Tree listing of files

![Alt devenvironemnt](devenvironment.png)
#### Basic Vim and iTerm keys for panes and window tabs
##### iTerm keyboard shortcuts
```
// to toggle iTerm terminal
press Opt/Alt + Space

// open new pane
press Cmd + d

// close a pane
press Cmd + w

// switch panes
press Cmd + { or }

// open new tab
press Cmd + t

// close a tab
press Cmd + w

// switch tabs
press Shift & Cmd + { or }

// highlight text w/o mouse for a copy and text
press Cmd + F
type in the text
press Tab to move forward
press Shift + Tab to move backward
press Cmd + F to close search box

```
##### Vim keybaord shortcuts
```
// to open Tree Listing navigation
:E

// open a pane/file vertically
press v

// close a pane/file
:q

// switch panes
press Ctrl + h/j/k/l

// resize panes
press Shift + h/j/k/l

// search a text in a pane/file
:/text here
```
##### Commandline 
```
// to search through files like Sublime-ish style
grep -rnC2 "text here" directory_here/

// search and replace
grep -rl matchstring somedir/ | xargs sed -i 's/string1/string2/g'
// sample
grep -rl 'windows' ./ | xargs sed -i 's/windows/linux/g'
```
##### Git Tig
```
tig // to open git tig
press Shft + s // to view un/staged files
press u // to toggle files to be staged or unstaged
press q // to quit view
press Shft + c // to commit and write commit msg
```

<hr>

### Setting up a local server with Node.js for Front-End Development
#### Using NPM for Package Manager
1. Install Home Brew first
2. and then install Node.js using brew
```
brew install node
```
3. to view installed packages in Brew
```
brew list
```
4. Use NPM to install Package Managers, Task Runners, Compilers, Preprocessors, etc
```
// to install
sudo npm install -g name_here

// to view package list
npm list -g --depth=0
```
* I use Yeoman.io to install web scaffoldings, very useful tool to get up and running with creating your web app!

<hr>

Tasks | Vim | Tmux | Terminal
--- | --- | --- | ---
Key-Bind | Ctrl | Alt/Option + A | Cmd
Open new pane | v | d | d
Open new window | - | t | t
Navigate through panes | h,j,k,l | Left, Right | [, ]
Navigate through windows | - | [, ] | Left, Right
Scoll in pane | Shift + [, ] | Page Up, Page Down for quick nav. For per line is arrows Up, Down | Shift + Page Up, Page Down
Exit of of Scroll pane mode | - | press Enter | -
Close a pane | :q | e | w
Close a window | - | w | w
Resize pane | Shft + hjkl | h, l | -
