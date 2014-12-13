vim-hykw-findAlternateFile
==========================

Vim command like "Find Alternate file" command in Emacs

It's to small snippets, I stopped to write a plugin, but defined in .vim file like below:

```vim
command! -nargs=1 -complete=file FindAlternateFile call <sid>Hykw_findAlternateFile(<q-args>)
function! Hykw_findAlternateFile(file)
  let current_bufferNumber = bufnr('%')
  execute "edit " . a:file
  execute "bdelete " . current_bufferNumber
endfunction
```

When you use the function, just type ":FindAlternateFile" in ex mode.
