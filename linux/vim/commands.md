# Vim Commands

## Basic

[Reference](https://missing.csail.mit.edu/2020/editors/) 

### Normal Mode
k - move up
j - move down
l - move right
h - move left

w - move forward by word
b - move backwards by a word

`shift + {` -  move up by a paragraph
`shift + }` - move down by a paragraph

yy - yank line
p - paste below
`shift + p` - paste above
dd - delete line 
u - undo last command
dw - delete word

`f + <char>` Forward jump to next instance of character (Use shift to move backwards, `;` to move forward through results, `,` to move backward through results)
`t + <char>`  Forward jump up to next instance of character 
x - delete single character 
s - delete single character and go into insert mode

`shift + d` - delete rest of line
`shift + c` - delete rest of line and go into insert mode
`shift + s` delete line and go into insert mode

**Note:** You can chain commands as follows
`dt)` - delete up to closing paranthensis

gg - go to top
`shift + g` - go to bottom
`<number>gg` - go to that line

In general, `<number><command>` will execute that command that many times:
`4w` - move forward 4 words
`12j` move down 12 lines

`shift + %` jumo to matching {},[],() pair
`yi shift + {` yank up to matching }

`ctrl + ^` - jump between open files

**Indenting:**
Start at the first line you want to indent, then press > and type the number of lines you want to indent and press > again (for 10 lines you'd press >10>) To un-indent you'd just use < instead of > (<10<)

## Visual Line Mode 
Highlight line by line (highlight lines)

Visual Line Mode - shift + v
y - yank highlighted
d - delete highlighted 
p - paste highlighted

(shift + .) - tab all selected lines

### Visual Mode
Highlight as you navigate (highlight words)

Visual Mode - v
y - yank highlighted
d - delete highlighted 
p - paste highlighted

(shift ") + (shift +) + (y) - yank to system register selected code 

### Insert Mode
Insert mode - i
`shift + i`  - insert mode to the beginning of the line
`shift + a`  - insert mode to the end of the line
Insert mode line below - o
Insert mode line above - shift + o
Escape insert mode - esc, crtl + c, ctrl + [ 

### Command Mode
command mode - :
/ - search mode (type what to search for), forward hop through results using `n`, backword hop through results using `shift + n`
`*` - search fo current word highlighted
`:noh` - clear last search results

`:e <path to file>` - find and open file
`:bd` - close currently open file
`:bn` - go to next open file
`:bp` - go to previous open file

`:%s/foo/bar/g`
Find each occurrence of 'foo' (in all lines), and replace it with 'bar'.
`:%s/foo/bar/gc`
Change each 'foo' to 'bar', but ask for confirmation first.

### Notes