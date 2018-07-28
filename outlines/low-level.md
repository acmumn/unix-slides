# Unix Classes Low-level Outline

## Overall

 - Each lesson starts with `git clone`ing a repo for that lesson.
 - The general structure of each top-level bullet point is:
   - ~5 minutes of whiteboard/theoretical explanation
   - ~5 minutes of us doing examples in the terminal
   - ~5 minutes where students are given a "challenge" to solve

## Lecture 1: Shell Basics

 - SSH
   - First 10-20 minutes of class are gonna be us walking people through how to
     connect to CSELabs on various systems.
   - OpenSSH on Unix, PuTTY on Windows
   - We're discouraging Vole, since GUIs make you weak.
 - `cd`, `ls`, `pwd`
   - Theory: The FS is a tree, absolute and relative paths, `~`
   - Example: Probably just some directory traversals, followed by `pwd`/`ls`
   - Challenge: Find the files in the `lecture-1/foo/bar` directory.
 - `less`, `man`
   - Theory: What does "pager" mean, `j`/`k`/`q` keybinds, the importance of
     rtfm-ing
   - Example: `man less`, `man 2 creat`, `less`ing some text file
   - Challenge: What does `printf`'s return value mean?
     - TODO: We don't teach C until 2021; is there a better example?
     - TODO: Ensure Nathan doesn't give a rant about how 19xx should be C and
       Scheme.
 - `cat`, `nano`, `fgrep`
   - NOTE: We're teaching `fgrep` to avoid spending time teaching regexes now.
   - Theory: Not much, other than noting that `grep` exists, and suggesting
     reading the manpage if one wants to learn now.
   - Example: `grep foo large-text-file.txt`, `nano buggy.c`, `cat short-file`
   - Challenge: Change `hello_world.py` to print `"Goodbye, world"` instead,
     using only the CLI.

## Lecture 2: Git and GitHub

This lecture's a bit different, since it's almost all theory.
We're going to be suggesting people do the GitHub Git tutorial *before* this
lesson.

TODO: This might need revision; it might make sense to just turn the GitHub Git
tutorial into a lecture...

 - Merkle Trees
   - Theory: Explaining what the data structure is.
   - Example: I might make a visual example? Probably not though, UIs are
     effort.
   - Challenge: Stay awake.
 - Git Flow
   - Theory: Explaining the workflow, showing an example.
   - Example: I'll probably make a couple trivial changes (adding comments?) to
     a real project of ours (MinneHack backend?) on a feature branch, then have
     another instructor make some other changes on their own.
   - Challenge: Don't cringe at my use of higher-order functions in Go.
 - GitHub Issues, PRs, Projects
   - Theory: None, probably.
   - Example: I'll open an issue on the project above and add it to a project.
     Then, I'll open a PR for my changes while the other instructor does the
     same. I'll review his PR asking for some changes, which they'll make. I'll
     then merge the PR.
   - Challenge: None

## Lecture 3: Vim

 - Basics: `hjkl`, `i`, `R`, `<Esc>`
   - Theory: Brief explanation of modal editing
   - Example: Moving around and editing a random file (maybe the slides?)
   - Challenge: Change `hello_world.java` to print `"Goodbye, world"` instead,
     using vim.
 - Searching: `/` and regexes
   - Theory: I'll probably give a brief regex tutorial, probably just `()`, `.`
     and `+`/`*`/`?`.
   - Example: Search through `moby-dick.txt` for `(h.+ )+` until I find
     `"hell's heart"`?
   - Challenge: TODO, but some regex search
 - Locations: `0`, `$`, `n`, `f`/`F`
   - Theory: Explain that all cursor movements, whether `hjkl`, `fF`, etc. are
     treated more or less uniformly.
   - Example: Just move around a bunch :P
   - Challenge: TODO, but maybe none?
 - Editing commands: `d`, `c`
   - Theory: Some actions take arguments, just like functions. Also, the `gn`
     location/movement.
   - Example: Probably some minor editing. Also, show `cc`/`dd` and `C`/`D`.
   - Challenge: TODO, but just more editing
 - Composing commands (e.g. `c2f.`)
   - Theory: Locations can be modified too! Show numeric prefix, since that's
     the most useful imo.
   - Example: More minor editing!
   - Challenge: TODO, even more editing!
 - `.` and `;`
   - Theory: `.` = repeat last action, `;` = repeat last movement.
   - Example: Editing for the editing god
   - Challenge: TODO edit
 - Command mode: `:w`, `:q`, `:!shell command`, `:read !shell command`
   - Theory: lol commands are a thing? not much needed...
   - Example: `:read !cal 2018` is a nice one, maybe that?
   - Challenge: Starting with an empty file, put a 2019 calendar in it and
     replace your birthday with `XX`. See how few keystrokes you can use!
 - Customizing Vim
   - Theory: Show them vimrc
   - Example: Show them my Vim setup (191 lines in vimrc, so not *that*
     ridiculous)
   - Challenge: Install vim-plug and go through vimawesome.com... at home :P

## Lecture 4: Pipes and Filters

First priority is gonna be a refresher on regexes, along with teaching `^`,
`$`, `[]`/`[^]`, and `{}`.

Then, a disclaimer that all of the filters are a lot more powerful than we're
presenting, and that you should check the manpages if you care.

Next, the theory behind redirecting stdio with `<`/`>`, then pipes as a natural
extension of this.

I'll probably put up a cheat sheet of the different commands effects on one
piece of data, then do one big example involving going through a 200MB log
file to try to find how attackers got control of one of our servers (this is a
fictitious scenario, plz no revoke network privileges).

 - `cut`
   - We're probably just going to cover `-c` and `-f`.
   - Example: Trim down a logfile to just status, method, and path.
 - `grep`
   - Mention that there are multiple regex standards, and that my method is to
     just add and remove backslashes until it works.
   - Example: Search for just errors with `^[45][0-9]{2} `.
 - `sed`
   - I'm just going to cover `s//`, since idk any other sed commands.
   - Example: TODO
 - `sort`
   - Sorting the errors by kind seems logical, idk.
 - `tr`
   - Example: TODO
 - `uniq`
   - Could go with `sort` once we realize there's way too many things to go
     through.
   - `uniq -c` is probably more useful than plain `uniq` here.
   - Mention `sort -u`, but don't use it.
 - `comm`
   - Maybe use this to compare a "normal" day's logs to the day of the
     intrusion?

I'm not sure what'd make a good challenge; maybe add `find` and `spell` to the
list of programs and have them make a oneliner to find the most commonly
misspelled words in a corpus?

## Lecture 5: (TENTATIVE) Customization

This one might be web-only, since it's basically just me talking at the viewer
and showing them how to set (some) things up.

 - Alternative Shells
   - fish
   - zsh
     - grml-zsh-config
     - oh-my-zsh
     - zsh-syntax-highlighting
 - Editors
   - neovim
   - vim-plug
     - Nathan's favorite plugins
   - any other editors we can find an instructor for
     - idk how to emacs, but we can probably find someone
     - does anyone use joe?
 - Sessions/Persistence
   - tmux
     - tpm, tmux-continuum, etc.
   - screen, if we can find an instructor
 - Replacements for standard tools
   - exa over ls
   - fd over find
   - nvimpager over less
   - ripgrep over grep
   - tealdeer/tldr over man
   - trash over rm
