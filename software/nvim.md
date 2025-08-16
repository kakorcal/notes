## Shortcut summary

1. `n ctrl+w+v` = [wincmd] vertical screen split
2. `n ctrl+w+s` = [wincmd] horizontal screen split
3. `n ctrl+w+w` = [wincmd] toggle between screen splits
4. `n ctrl+h|j|k|l` = [wincmd] toggle between screen splits in a specific direction
5. `n <leader>sf` = [telescope] search for file
6. `:help [package]` = [vim] open manual for package
7. `n gr` = [mason-LSP] go to function reference
8. `ctrl+q` = [telescope] add result to quickfix list
9. `n <leader>qo` = [custom-vim] open quickfix list (a list of filename and location). replaces `:copen`
10. `n <leader>qc` = [custom-vim] close quickfix list. replaces `:cclose`
11. `n shift+8` = [hlsearch] highlight all instances of the word on cursor
12. `n %` = [vim] toggle between 'kalsdjfodsaif' brackets {} [] ()
13. `n f|t<letter>` = [vim] jump to (for f) or before (for t) a letter. `;` to go to next instance and `,` to go back 
14. `n d|c|y+a` = [nvim] delete or yank everything inside and including the text. Most useful options are `w` (word), `'` (string), `{` (bracket)
15. `n d|c|y+i` = [nvim] delete or yank everything inside and excluding the text. Most useful options are `w` (word), `'` (string), `{` (bracket)
16. `ctrl+^` = [nvim] go to previous buffer
17. `:so $MYVIMRC` = [nvim] reboot source file. In this case it is init.lua
18. `n <leader>q` = [nvim] open diagnostics quickfix list
19. `n <leader>sd` = [telescope] open diagnostics search list
20. `n \` = [treesitter] toggle treesitter file explorer side nav
21. `:Mason` = [mason-LSP] show installed LSPs
22. `n <leader>qk` = [custom-cloak] toggles cloak. replaces `:CloakToggle`
23. `n <leader>sw` = [telescope] search for word
24. `n [c` = [nvim] go to next git change
25. `n <leader>qn` = [custom-vim] go to next line in quickfix list. replaces `:cnext`
26. `n <leader>qp` = [custom-vim] go to previous line in quickfix list. replaces `:cprev`
27. `ctrl+o|i` = [vim] go next/previous of jumplist. use `:jumps` to see the full list
28. `n <leader>st` = [custom-telescope] search for git files
29. `shift+k` = [mason-LSP] show type and/or function signature
30. `:%s/<regex>/<replacement>/<options>` = [vim] search and replace entire file. Tip: use \(.\) to capture a group then reference it with \1..n
31. `:'<,'>s/<regex>/<replacement>/<options>` = [vim] search and replace highlighted texts. Tip: use ^ for beginning of line and $ for end of line additions

-- Todo
fork kickstart in order to push into my own repo
edit all highlighted texts at once
format code with proper indentation
adding, removing, renaming files and folders
reindex numbers
node debugger
tmux commands (going back and forth projects)
git diff shower (fugitive)
closing all files and opening new ones
handling other languages like Japanese or Spanish

## vim

#### f command to jump to a letter
Use f and press a letter. : to go to the next instance of the letter and comma to go back

#### c (change) command
Deletes specified text and goes into insert mode

#### ctrl ^
Edits the alternate file. Effectively you can toggle between a previously edited file. Useful when using telescope

#### Toggling between brackets
Highlight over a bracket then press % to toggle



## nvim

#### press ctrl w to open window navigation
You can navigate between split windows

#### use :split <filename> or :vsplit <filename> for split screen
Or you can use control wv to split vertically then use telescope to search for a file on that buffer

#### use :so to reboot nvim
This is the same as using the source command



## nvim kickstart init.lua settings

#### nvim will automatically copy to your clipboard when yanking
```
-- Sync clipboard between OS and Neovim.
--  Schedule the setting after `UiEnter` because it can increase startup-time.
--  Remove this option if you want your OS clipboard to remain independent.
--  See `:help 'clipboard'`
vim.schedule(function()
  vim.opt.clipboard = 'unnamedplus'
end)
```

#### nvim shortcut to highlight all instances of text in normal mode and pressing *
```
-- Clear highlights on search when pressing <Esc> in normal mode
--  See `:help hlsearch`
vim.keymap.set('n', '<Esc>', '<cmd>nohlsearch<CR>')
```

#### vim.keymap.set can accept functions
```
-- in this example, if you press 'he', it will print hello to your console
vim.keymap.set('n', 'he', function() print('hello') end)
```

#### Diagnostic keymap
```
-- Diagnostic keymaps
vim.keymap.set('n', '<leader>q', vim.diagnostic.setloclist, { desc = 'Open diagnostic [Q]uickfix list' })
```

#### Opening diagnostic menu
You can open diagnostic menu with [ or ]

#### Telescope bindings
```
      -- See `:help telescope.builtin`
      local builtin = require 'telescope.builtin'
      vim.keymap.set('n', '<leader>sh', builtin.help_tags, { desc = '[S]earch [H]elp' })
      vim.keymap.set('n', '<leader>sk', builtin.keymaps, { desc = '[S]earch [K]eymaps' })
      vim.keymap.set('n', '<leader>sf', builtin.find_files, { desc = '[S]earch [F]iles' })
      vim.keymap.set('n', '<leader>ss', builtin.builtin, { desc = '[S]earch [S]elect Telescope' })
      vim.keymap.set('n', '<leader>sw', builtin.grep_string, { desc = '[S]earch current [W]ord' })
      vim.keymap.set('n', '<leader>sg', builtin.live_grep, { desc = '[S]earch by [G]rep' })
      vim.keymap.set('n', '<leader>sd', builtin.diagnostics, { desc = '[S]earch [D]iagnostics' })
      vim.keymap.set('n', '<leader>sr', builtin.resume, { desc = '[S]earch [R]esume' })
      vim.keymap.set('n', '<leader>s.', builtin.oldfiles, { desc = '[S]earch Recent Files ("." for repeat)' })
      vim.keymap.set('n', '<leader><leader>', builtin.buffers, { desc = '[ ] Find existing buffers' })

```

#### Moving around split windows with control hjkl
```

vim.keymap.set('n', '<C-h>', '<C-w><C-h>', { desc = 'Move focus to the left window' })
vim.keymap.set('n', '<C-l>', '<C-w><C-l>', { desc = 'Move focus to the right window' })
vim.keymap.set('n', '<C-j>', '<C-w><C-j>', { desc = 'Move focus to the lower window' })
vim.keymap.set('n', '<C-k>', '<C-w><C-k>', { desc = 'Move focus to the upper window' })

```

#### Which-key gives you a guide on available key bindings as you type. You can disable once you get used to the commands
Yanking and deleting. y or d opens a menu to do more selections. For example, yap will yank around paragraph

#### nvim kickstart uses lazy as its package manager
Lazy will autosource all files in a specified directory

#### nvim packages you can look into
```
cloak
fugitive
undotree
harpoon
```

#### Mason is a LSP specific package manager
You can type `:Mason` to see and manage your current LSP tools. Then you can uninstall by pressing X over the tool. Or you can use U to update

#### Finding function references
Type gr over a function to find references. The LSP will find it then pipe into telescope. Open quickfix list by typing in ctrl + q. Quickfix list is just a list of references that persist even after closing the buffer. You can go to the next list item in the quickfix list with `:cnext` or `:cprev`

#### Treesitter
Type \ to toggle side nav

#### Resources
https://www.youtube.com/watch?v=-ybCiHPWKNA
https://www.youtube.com/watch?v=w7i4amO_zaE
