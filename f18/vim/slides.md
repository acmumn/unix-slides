Vim!
----

Or, The Power of Modal Editing

---

### SSH into CSELabs

<img src="https://imgur.com/DQFGvXn.png"></img>

---

```
ssh X500@csel-khROOM-NUM.cselabs.umn.edu

X500 = Your Internet ID
ROOM = 1250, 4240, 4250
NUM = 01 .. 20
```

---

Then go get pizza!

---

### What is Modal Editing?

> Pressing one button would put your car into a mode where the steering wheel was connected to the rest of the steering mechanism. Pressing another button would put your car into another mode where it would control the radio dial. It would be impossible to steer and change stations at the same time.
>
> -- WikiWikiWeb's `IfYourCarWereVim` Article

---

### The Modes of Vim

-	Normal
-	Insert
-	Replace
-	Command

---

### Normal Mode

-	Movement with `hjkl`

---

#### The ADM-3A Terminal

![](http://imgur.com/S4kbdjA.png)

---

![](http://imgur.com/bzdCXEf.png)

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`

---

### Searching

-	Use `/` to search by regex

---

#### Regexes

-	**Reg**ular **Ex**pressions

---

#### Regexes

-	**Reg**ular **Ex**pressions
-	Metacharacters
	-	`.` -- Any Character
	-	Repeats
		-	`?`: 0-1
		-	`*`: 0-&infin;
		-	`+`: 1-&infin;
	-	`[pq]` -- P or Q
	-	`[a-z]` -- Any lowercase letter
	-	`()` for grouping
	-	`|` is "or"

---

#### Regex Examples

-	`b(an)*` matches:
	-	`b`
	-	`ban`
	-	`banan`
	-	but not `banana`
-	`b[an]*` matches `banana`, but not `ban ann`
-	`b[ an]+` matches `banana` and `ban ann`, but not `b`

---

#### Regex Problem

-	What regex matches both `purge` and `forge`?
-	What strings match `[abc][de]+`?

---

### Locations in Vim

-	Beginning of Line: `0`
-	End of Line: `$`
-	Next Search Result: `gn`

---

### Composite Vim Commands

```
(repetitions)(base command)(location)?
```

-	`[repetitions]` might be
-	`[base command]` might be `c` or `d`
-	`[location]` might be `$`, `j` or `gn`

---

### More Normal Mode Commands

-	Delete with `d`

---

### More Normal Mode Commands

-	Delete with `d`
-	Change with `c`

---

### More Normal Mode Commands

-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`

---

### More Normal Mode Commands

-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`

---

### More Normal Mode Commands

-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`
-	"Yank" (copy) with `y`
-	Paste with `p`

---

### More Normal Mode Commands

-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`
-	"Yank" (copy) with `y`
-	Paste with `p`
-	Undo with `u`
-	Redo with `^r`

---

### More Normal Mode Commands

-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`
-	"Yank" (copy) with `y`
-	Paste with `p`
-	Undo with `u`
-	Redo with `^r`
-	Repeat last command with `.`

---

### Command Mode

-	Hit `:`
-	`:w` to save

---

### Command Mode

-	Hit `:`
-	`:w` to save
-	`:q` to quit

---

### Command Mode

-	Hit `:`
-	`:w` to save
-	`:q` to quit
-	`:wq` to save and quit

---

### Command Mode

-	Hit `:`
-	`:w` to save
-	`:q` to quit
-	`:wq` to save and quit
-	`:r <path>` to read in a file

---

### Command Mode

-	Hit `:`
-	`:w` to save
-	`:q` to quit
-	`:wq` to save and quit
-	`:r <path>` to read in a file
-	`:r !<cmd>` to read in the output of a command

---

### Command Mode

-	Hit `:`
-	`:w` to save
-	`:q` to quit
-	`:wq` to save and quit
-	`:r <path>` to read in a file
-	`:r !<cmd>` to read in the output of a command
-	`:e <path>` to open a file

---

### Command Mode

-	Hit `:`
-	`:w` to save
-	`:q` to quit
-	`:wq` to save and quit
-	`:r <path>` to read in a file
-	`:r !<cmd>` to read in the output of a command
-	`:e <path>` to open a file
-	`:bn` to go the the **n**ext **b**uffer
-	`:bp` to go the the **p**revious **b**uffer
-	`:bd` to **d**elete (close) the current **b**uffer

---

### Learning More

-	`:help`
-	`vimtutor`
