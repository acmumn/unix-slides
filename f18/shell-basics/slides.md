# Shell Basics

---

### SSH into CSELabs

#### Windows

Get a client (PuTTY / MobaXterm)

-----

#### Linux/macOS

Just open a terminal and type

```bash
ssh X500@csel-khROOM-MACHINE.cselabs.umn.edu

# X500 = Your Internet ID
# ROOM = 1200, 1250, 4240, 4250
# MACHINE = 0 ... 20
```

-----

Then go get pizza!

---

Get the class files

```bash
git clone https://github.umn.edu/TODO/lesson-1.git

# -or-

git clone git@github.umn.edu:TODO/lesson-1.git
```

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

Any file that starts with a dot (`.`) is a _hidden file_.

Show hidden files with `-a`.

<table><thead>
<tr><th>Without <pre>-a</pre></th><th>With <pre>-a</pre></th></tr>
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

List the files inside `lesson-1/foo/bar`

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

(See demonstration.)

NOTE: Demo `less the-old-man-and-the-sea.txt`; `j`, `k`, `q`, `/` keybinds.

---

##### Try it yourself

Read the files in `lesson-1/foo/bar` using the terminal!

---

`man` is a viewer for **man**ual pages

This is mainly good when you want to know how to use a tool, or a C library function.

NOTE: Demo `man less`, `man creat`

---

##### Try it yourself

How do we get searches in `less` to be case-insensitive?
(Find the answer in `man less`.)

---

`fgrep` allows searching for strings in a file.

NOTE:
State that it's a simpler version of the more powerful `grep`, which we'll discuss later.
Demo searching for `DiMaggio`.

---

##### Try it yourself

Pedrico gets a gift -- what is it?

---

`nano` is a (pretty crap [cue angry Louis]) text editor.

---

##### Try it yourself

Change `hello_world.py` to instead print `Goodbye, world!`
