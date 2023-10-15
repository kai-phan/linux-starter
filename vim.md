# VIM

## Fire up
```bash
$ vim README.md
```

### Search pattern, in Vim session, 
- type `/` and then type the pattern, e.g. `linux-starter`.
Once the pattern is found, press `n` to go to the next match. Press `N` to go to the previous match.
- Type `?` to search backward.

[//]: # (- Type `*` to search the word under the cursor.)
[//]: # (- Type `#` to search the word under the cursor backward.)

### Navigate
- `h` : left
- `j` : down
- `k` : up
- `l` : right
- `w` : next word
- `b` : previous word
- `0` : beginning of line
- `$` : end of line
- `gg` : beginning of file
- `G` : end of file
- `H` : top of screen
- `M` : middle of screen
- `L` : bottom of screen
- `Ctrl + f` : forward one screen
- `Ctrl + b` : backward one screen
- `Ctrl + d` : forward half screen
- `Ctrl + u` : backward half screen
- `Ctrl + e` : scroll down one line
- `Ctrl + y` : scroll up one line

### Insert
- `i` : insert before cursor
- `a` : append after cursor
- `o` : open a new line below the current line
- `O` : open a new line above the current line
- `r` : replace one character

### Edit
- `x` : delete one character
- `X` : delete one character before cursor
- `y` : yank
- `yw` : yank word
- `yy` : yank line
- `Y` : yank to the end of line
- `dw` : delete one word
- `dd` : delete one line
- `D` : delete to the end of line
- `u` : undo
- `Ctrl + r` : redo
- `.` : repeat last command
- `p` : paste after cursor
- `P` : paste before cursor
- `J` : join lines
- `c` : change
- `cw` : change word
- `cc` : change line
- `C` : change to the end of line
- `s` : substitute
- `S` : substitute line
- `r` : replace one character
- `R` : replace mode
- `~` : switch case
- `<<` : shift left
- `>>` : shift right
- `=` : auto indent
- `==` : auto indent line
- `>` : indent
- `<` : unindent

### Save and quit
- `:w` : write
- `:q` : quit
- `:wq` : write and quit
- `:q!` : quit without saving
- `:u`: undo