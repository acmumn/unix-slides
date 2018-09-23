Vim!
----

Or, The Power of Modal Editing

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
	-	Repeats
		-	`?` -- 0-1
		-	`*` -- 0-&infin;
		-	`+` -- 1-&infin;
	-	`.` -- Any Character
	-	`[pq]` -- P or Q
	-	`[a-z]` -- Any lowercase letter
	-	`()` for grouping
	-	`|` is "or"

---

#### Regex Examples

-	`b(an)*` matches:
	-	`b`
	-	`ban`
	-	`banana`
	-	but not `banann`
-	`b[an]*` matches `banann`, but not `ban ann`
-	`b[ an]+` matches `ban ann`, but not `b`

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

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
-	Delete with `d`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
-	Delete with `d`
-	Change with `c`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`
-	"Yank" (copy) with `y`
-	Paste with `p`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
-	Delete with `d`
-	Change with `c`
-	Delete one character with `x`
-	Substitute with `s`
-	"Yank" (copy) with `y`
-	Paste with `p`
-	Undo with `u`
-	Redo with `^r`

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`
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
