# Shell Basics

---

### SSH into CSELabs

#### Windows

 - Download a client
   - Nathan recommends PuTTY
   - Michael recommends MobaXterm

-----

#### Linux/macOS

Just open a terminal and type

```bash
ssh X500@csel-khROOM-MACHINE.cselabs.umn.edu

# X500 = Your Internet ID
# ROOM = 1200, 1250, 4240, 4250
# MACHINE = 0 ... 20
```

---

```bash
git clone https://github.umn.edu/ringo025/unix-4.git

# -or-

git clone git@github.umn.edu:ringo025/unix-4.git
```

-----

Then go get pizza!

---

## Navigating the Filesystem

---

The filesystem is a tree, with files and directories.

```
/
  bin/
  home/
    you/
      Documents/
        file.txt
    someone_else/
  usr/
```

---

Every process has a "current" directory. You can probably see it in your shell:

```
  /
    bin/
    home/
*     you/ (also known as ~)
        Documents/
          file.txt
      someone_else/
    usr/
```

(Note: shells usually start in your home directory.)

---

`cd` means **c**hange **d**irectory.

```
  /
    bin/
    home/
      you/
*       Documents/
          file.txt
      someone_else/
    usr/
```

---

`ls` is short for **l**i**s**t.

```
```

---

  absolute and relative paths, `~`, `.`, and `..`, Hidden Files
 - `cd`, `ls`, `pwd`
   - Example: Probably just some directory traversals, followed by `pwd`/`ls`
   - Challenge: Find the files in the `lecture-1/foo/bar` directory.

---

 - `less`, `man`
   - Theory: What does "pager" mean, `j`/`k`/`q` keybinds, the importance of
     rtfm-ing
   - Example: `man less`, `man 2 creat`, `less`ing some text file
   - Challenge: What does `printf`'s return value mean?
     - TODO: We don't teach C until 2021; is there a better example+challenge than `creat`+`printf`?
     - TODO: Ensure Nathan doesn't give a rant about how 19xx should be C and
       Scheme.

---

 - `cat`, `nano`, `fgrep`
   - Theory: Not much, other than noting that `grep` exists, and suggesting
     reading the manpage if one wants to learn now.
   - Example: `grep foo large-text-file.txt`, `nano buggy.c`, `cat short-file`
   - Challenge: Change `hello_world.py` to print `"Goodbye, world"` instead,
     using only the CLI.
