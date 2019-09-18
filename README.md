# Git 101

Tutorial repo used to demonstrate / practice some [git ](https://git-scm.com/) / [github.com](https://github.com) basics.

## Configuration

To set the username and email that will be displayed in all your commits, use the following commands:

```33 bash
git config user.name "your name here"
git config user.email "usename@domain.com"
```

## Creating a README File

This file is known as a README file and can be used as a means to document / communicate things about your code. [Markdown](https://en.wikipedia.org/wiki/Markdown) is the common format used for README files, and is the format that [github.com](https://github.com) recognizes and renders as html in your repo's homepage.

### Typora

![Image of the Typora "misty theme."](https://theme.typora.io/media/thumbnails/misty-theme.png)

One of the simplest ways to create / edit Markdown files is to use [Typora](https://typora.io/).

> Typora will give you a seamless experience as both a reader and a 
> writer. It removes the preview window, mode switcher, syntax symbols of 
> markdown source code, and all other unnecessary distractions. Replace 
> them with a real live preview feature to help you concentrate on the 
> content itself.

### Markdown Cheat Sheet

If you wish to learn the Markdown syntax this [cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) should serve as a good reference.



## Git Commands

### init

Creates a git repo of all the contents in the current directory.

```bash
git init
```

*Note: This does not automatically add all files to the repo, it simply creates the .git directory which lets Git know that the current directory is to be treated as a repo.*

### status

```bash
git status
```

This command allows you to see the status of your repo by displaying a list of files which have either changed, been deleted, or have yet to be added to the repo.

### diff

```bash
git diff <path to file>
```

Shows which lines of code have been modified since the last commit.

### add

```bash 
git add <path to file>
```

This command "stages" the file so that it will be committed to the repo the next time the *git commit* is executed.

### commit

Commits the changes made to all files which have been staged. All commit require a message in order to execute. Messages serve as a summary or note of the changes that have been made to the files being staged. Although many files can be staged at one time, it is recommended that only one file, or related files, be committed at a time. Doing so will make reverting changes easier and it will make it easier for others to keep track of file changes.

#### -m flag

Commits the staged files using the message typed within the quotation marks. Good for short commit messages.

```bash
git commit -m "your commit message here..."
```

#### -F flag

There are times when a more detailed commit message is necessary. In those instances, the commit message can be written to a text file. That file can then be referenced using this flag. Git will 

[]: 

parse the file and it's contents will be set as the commit message.

```bash
git commit -F <path to commit message file>
```

### remote add

```bash
git remote add ...
```

# Platform Specific Recommendations

These recommendations are based solely on my personal opinion / experience. Always adhere to what works best for you and your workflow.

## Windows 

### cmder

![cmder main image from website.](https://cmder.net/img/main.png)

[Cmder](https://cmder.net/) is a console emulator which can serve as a good alternative to the Windows Command Prompt (cmd). Cmder allows you to use common unix commands like ls, rm, etc. It also comes with console applications like nano, vim, and git, pre-installed.

>Cmder is a software package created out of pure frustration over the absence of nice console emulators on Windows. It is based on amazing software, and spiced up with the Monokai color scheme and a custom prompt  layout, looking sexy from the start.                 

[]: https://cmder.net/

### Windows Sub-system for Linux (WSL)

Using WLS for editing files / managing a git repo can cause conflicts with line-endings. Linux uses LF while windows uses CLRF. This will lead to error when parsing, compiling, or editing code. To prevent conflicts, one must be consistent in the development platform being used. Either do all editing / compiling in WSL or on Windows. Otherwise, a manual change of line-endings for all files must be performed.



## Linux | MacOS

### Oh My Zsh

> [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh) is a delightful, open source, community-driven framework for 
> managing your Zsh configuration. It comes bundled with thousands of 
> helpful functions, helpers, plugins, themes, and a few things that make 
> you shout...

#### Agnoster Theme

![agnoster](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

A favorite theme to use with Oh My Zsh is Agnoster. To set this theme, simple edit your ~/.zshrc file:

```bash
ZSH_THEME="agnoster"
```

It requires the installation of [Powerline Fonts](https://github.com/powerline/fonts).


