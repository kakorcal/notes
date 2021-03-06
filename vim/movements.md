# Horizontal movement
1. i - insert to left of cursor
2. a - insert to right of cursor 
3. shift+i - insert from start of line
4. shift+a - insert from end of line
5. l - move right one space
6. h - move left one space
7. 0 - jump to start of line
8. _ - jump to start of non whitespace content
9. $ - jump to end of line
10. c - equivalent to d but goes into insert mode afterwards
11. C - delete everything on right side of cursor and go to insert mode
12. c0 - delete everything on left side of cursor and go to insert mode
13. S - delete entire line and go into insert mode
14. s - delete character and go into insert mode
15. f - move to the first occurrence of the next letter typed. Use ; to go forward and , to go back 
16. t - move to the letter before the first occurrence of the next letter typed. Use ; to go forward and , to go back 

# Vertical movement
1. gg - go to top of file
2. G - go to bottom of file
3. o - insert from start of next line
4. shift+o - insert from start of previous line
5. j - move down one space
6. k - move up one space
7. { - move up one paragraph
8. } - move down one paragraph
9. % - move to the next bracket pair then toggle (),[],or{}

# Basic commands
1. y - yank
2. d - delete
3. r - replace
4. o - opens to newline then to insert mode
5. a - goes to insert mode after line
6. p - paste
7. c - change to insert mode after deleting
8. s - sentance. goes to insert mode after deleting
9. <ctrl-r> - redo
10. u - undo
11. r - replace. Type r then type the next character that will replace the existing one

# Combos
1. dG - delete everything from cursor to bottom of file
2. ggdG - delete everything in file
3. dtLETTER - delete up to but not including the letter inputted
4. dfLETTER - delete up to the letter inputted
5. SHIFTvBRACKET%d - delete a code block
6. diPAIRS - delete everything between pairs of brackets or strings. Recommend cursor to be inside the pair but for some reason it works for strings if cursor is outside: 
7. ciPAIRS - same thing as diPAIRS except it goes into insert mode afterwards
8. viPAIRS - same thing as diPAIRS except it goest into visual mode afterwards
9. daPAIRS - delete everything between pairs of brackets or strings including the bracket or string. Recommend cursor to be inside the pair but for some reason it works for strings if cursor is outside
10. caPAIRS - same thing as daPAIRS except it goes into insert mode afterwards
11. vaPAIRS - same thing as daPAIRS except it goes into visual mode afterwards
12. vaBRACKETSSHIFTv - hightlight entire code block
13. yiPAIRS - same thing as diPAIRS except it yanks the text
14. viw - highlight word from within the word
15. viW - highlight word including symbols until the whitespace from within the word
16. Y - yank enter line. When pasting it will paste on newline
17. d$ - delete right side of line from cursor
18. d0 - delete left side of line from cursor

# Misc
* [Link to cheatsheet](https://vim.rtorr.com/)
* [Link to vim course](https://frontendmasters.com/courses/vim-fundamentals/advanced-motions-horizontal-vertical-movement/)
