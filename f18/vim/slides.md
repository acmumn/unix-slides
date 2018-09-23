Vim!
----

Or, The Power of Modal Editing

---

### What is Modal Editing?

> Every once in a while, a mistaken sequence of actions will result in someone entering 'non-visual mode'; all the windows go blank, and a directional sonar pops up.
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

![](http://www.catonmat.net/images/why-vim-uses-hjkl/lsi-adm-3a.jpg)

---

![](http://www.catonmat.net/images/why-vim-uses-hjkl/lsi-adm3a-full-keyboard.jpg)

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`

---

### Insert Mode

---

### Normal Mode

-	Movement with `hjkl`
-	Change to insert mode with `i`
-	Change to replace mode with `R`

---

### Replace Mode

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
-	`[location]` might be `$` or `gn`

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
-	Repeat last command with `.`

---

### Command Mode

-	Hit `:`
-	e.g. `:w`, `:q`, `:wq`
