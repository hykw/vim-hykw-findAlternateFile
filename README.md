vim-hykw-findAlternateFile
==========================

Vim command like "Find Alternate file" command in Emacs

It's to small snippets, I stopped to write a plugin, but defined in .vim file like below:

      command! -bar FindAlternateFile call Hykw_findAlternateFile() 
      function! Hykw_findAlternateFile()
        let current_bufferNumber = bufnr('%')
        let file = input('Find alternate file: ', '', 'file')
        execute "edit " . file
        execute "bdelete " . current_bufferNumber
      endfunction

When you use the function, just type ":FindAlternateFile" in ex mode.
