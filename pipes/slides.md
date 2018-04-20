## Unix Pipes and Filters

---

### What are Filters?

A filter is a program that accepts text in lines from stdin, and outputs text via stdout.

 - `cat`
 - `cut`
 - `grep`
 - `sed`
 - `sort`
 - `tr`
 - `uniq`

-----

### What are Pipes?

A pipe is a construct in the Unix shell that connects the output of one program to the input of another.

`cat the-entire-last-year.log | grep WARN | grep Security | cut -c 7-`

---

### Finding A Hidden Phrase

`problem1.txt` contains a secret password directly after the word `millionth`.

How do we find this?

-----

#### `cat`

`cat FILE...`

-----

#### `grep`

`grep REGEX`

---

### O Toxt Tronsformotoon Problom

`problem2.txt` contains some text, but the only real vowel is `o`.
How do we convert the text?

-----

#### `tr`

`tr FROM-CHARS TO-CHARS`

---

### EBG13 Genafyngvba

`problem3.txt` contains some text, but it's in code so we can't read it.
Luckily, since infosec is a silly myth, we know it's ROT13.

We want to search through it for the word `password`.

-----

#### What is ROT13

```
abcdefghijklmnopqrstuvwxyz
nopqrstuvwxyzabcdefghijklm
```

-----

#### How to translate ROT13?

 - `a-m` gets mapped to `n-z`
 - `n-z` gets mapped to `a-m`

---

### Find a non-duplicate Line

`problem4.txt` is a large text file with a bunch of text.

We want to find the line of text that doesn't occur twice.

-----

#### `sort`

`sort` sorts the files.

-----

#### `uniq`

`uniq` makes files locally unique.

-----

#### `uniq`

```
$ cat << EOF | uniq
asdf
asdf
qwerty
qwerty
qwerty
foo
asdf
```

-----

#### `uniq`

```
asdf
qwerty
foo
asdf
```

-----

#### `uniq -c`

```
$ cat << EOF | uniq -c
asdf
asdf
qwerty
qwerty
qwerty
foo
asdf
```

-----

#### `uniq -c`

```
2 asdf
3 qwerty
1 foo
1 asdf
```

---

# Questions?
