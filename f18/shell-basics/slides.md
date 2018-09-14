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

Shells usually start in your home directory.

---

`cd` means **c**hange **d**irectory.

`.` is the current directory, `..` is one directory up.

```
  /
    bin/
    home/
~      you/
..      Documents/
.         csci8991/
            file.txt
      someone_else/
    usr/
```

---

`ls` is short for **l**i**s**t.

```
file.txt
```

`ls -l` gives more information.

```
total 4
-rw-r--r-- 1 nathan nathan 1013 Sep 13 19:14 file.txt
```

---

Any file that starts with a dot (.) is a _hidden file_.

Show hidden files with `-a`.

<table><thead>
<tr><th>Without -a</th><th>With -a</th></tr>
</thead><tbody>
<tr><td><pre>Desktop
Documents
Pictures</pre></td><td><pre>.bash_history
.bash_profile
.bashrc
Desktop
Documents
Pictures
etc...
</pre></td></tr>
</tbody></table>

---

##### Try it yourself

Download the files and locate the files inside:

- `lesson-1/foo/bar`

---

cat: for con**cat**enate

```
$ cat hello.txt
hello!
```

---

##### Try it yourself

Print the contents of the files using the terminal!

---

man: manual pages

Don't need to search Google for everything

---

 - `cat`, `nano`, `fgrep`
   - Theory: Not much, other than noting that `grep` exists, and suggesting
     reading the manpage if one wants to learn now.
   - Example: `grep foo large-text-file.txt`, `nano buggy.c`, `cat short-file`
   - Challenge: Change `hello_world.py` to print `"Goodbye, world"` instead,
     using only the CLI.

---

`cat` writes files to standard output.

If you give it multiple files as arguments, it will con**cat**enate them.

```
$ cat hello.txt
Hello!
$ cat goodbye.txt
Goodbye!
$ cat hello.txt goodbye.txt
Hello!
Goodbye!
```

---

`less` is the pager, which is used to display long outputs in pages.

---

`less` is the pager, which is used to display long outputs in pages.

 - `less`, `man`
   - Theory: What does "pager" mean, `j`/`k`/`q` keybinds, the importance of
     rtfm-ing
   - Example: `man less`, `man 2 creat`, `less`ing some text file
   - Challenge: How do you make `grep` case-insensitive.
