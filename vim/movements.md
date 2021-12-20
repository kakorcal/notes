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
14. f - move to the first occurrence of the next letter typed. Use ; to go forward and , to go back 
15. t - move to the letter before the first occurrence of the next letter typed. Use ; to go forward and , to go back 

# Vertical movement
1. gg - go to top of file
2. G - go to bottom of file
3. o - insert from start of next line
4. shift+o - insert from start of previous line
5. j - move down one space
6. k - move up one space
7. { - move up one paragraph
8. } - move down one paragraph

# Combos
1. dG - delete everything from cursor to bottom of file
2. ggdG - delete everything in file
3. dtLETTER - delete up to but not including the letter inputted
4. dfLETTER - delete up to the letter inputted

# Misc
* [Link to cheatsheet](https://vim.rtorr.com/)
* [Link to vim course](https://frontendmasters.com/courses/vim-fundamentals/advanced-motions-horizontal-vertical-movement/)
