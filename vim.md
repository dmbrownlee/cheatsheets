# Vim Quick Reference
Main site: [vim.org](https://www.vim.org/)

## Vim modes
Mode | Description
--- | ---
normal | Vim starts in normal mode.  When in normal mode, each key does something.  For example, <code>d</code> deletes, <code>c</code> changes, <code>u</code> undoes the last edit, etc.
command | Typing <code>:</code> while in normal mode puts Vim in command mode.  In command mode, a line opens at the bottom of the screen with a <code>:</code> prompt and you can type commands for Vim to execute. Typing a command followed by the return key will run the command while pressing the [Esc] key will cancel command mode and return you to normal mode without running anything.
insert | When in insert mode, each character you type is input into the buffer. This is how most text editors work.  When you are done typing, press the [Esc] key to return to normal mode.
visual | Moving the cursor while in visual mode will mark a range of text.  Subsequent editing operations will work on that range of text.  Press the [Esc] key to cancel the visual selection and return to normal mode.
search | Similar to  command mode, search mode will put you on a line at the bottom of the screen where you can type the text you want to search for.  The prompt will be a <code>/</code> or <code>?</code> depending on whether you typed, while in normal mode, <code>/</code> to search from the cursor forward or <code>?</code> to search backwards from the cursor. Press the [Esc] key to cancel the search and return to normal mode.

## Starting Vim
command line| result
--- | ---
<code>vim           </code>|Opens vim with an empty buffer and no filename set.
<code>vim *filename*</code>|Opens vim with the file *filename* loaded into the buffer.</br>If *filename* does not exist, buffer is empty but filename is set and</br>will be created when the buffer is saved.
<code>vimtutor</code>|Opens vim with a copy of quick tutorial document you can edit while reading to help you get started using Vim.

## Saving changes and exiting Vim
from normal mode | result
--- | ---
<code>:q</code>| Closes (quits) the current buffer it ***if*** doesn't contain changes.</br>If this is the only buffer, vim exits.</br>If the current buffer has unsaved changes, displays a warning and does nothing.
<code>:q!</code>| Force closes the current buffer.</br>If this is the only buffer, vim exits.</br>If the current buffer has unsaved changes, they are discarded.
<code>:w</code>| Writes the current buffer to file ***if*** the buffer has an associated filename.</br>If the current buffer is not associated with a file, displays a warning and does nothing.
<code>:w!</code>| Force writes and closes the current buffer.</br>If the current buffer is not associated with a file, displays a warning and does nothing.</br>Forcing a write is only usful to overcome certain combinations of filesystem permissions and is normally not necessary.
<code>:wq</code>| Writes the current buffer to file before closing it ***if*** the buffer has an associated filename.</br>If this is the only buffer, vim exits.</br>If the current buffer is not associated with a file, displays a warning and does nothing.
<code>:wq!</code>| Force writes and closes the current buffer.</br>If this is the only buffer, vim exits.</br>If the current buffer is not associated with a file, displays a warning and does nothing.</br>Forcing a write is only usful to overcome certain combinations of filesystem permissions and is normally not necessary.

## Opening multiple files when starting Vim
shell command | result
--- | ---
<code>vim *file1* *file2* ...</code>|Opens vim with a single window and multiple files open in separate buffers.</br>Use <code>:n</code> and <code>:N</code> to go forward and backward between buffers.
<code>vim -O *file1* *file2* ...</code>|Opens vim with multiple, *vertical* windows, each with its on buffer containing a file.</br>Use <code>Ctrl-w,Ctrl-w</code> to cycle through the windows.
<code>vim -o *file1* *file2* ...</code>|Opens vim with multiple, *horizontal* windows, each with its on buffer containing a file.</br>Use <code>Ctrl-w,Ctrl-w</code> to cycle through the windows.
<code>vim -p *file1* *file2* ...</code>|Opens vim with a single window and multiple tabs, each with its own buffer containing a file.</br>Use <code>gt</code> and <code>gT</code> to go forward and backward between tabs.
