Title: vim Macro Cheatsheet
Date: 2012-08-25 17:33
Category: tools
Tags: vim, editor
Authors: Bhargav Bhat
Summary: Macro Cheatsheet for vim

_This is a suppliment to the earlier vim sesssions and was shared as an email to an internal team group_

#### Macros Recap

#### Macro Recording & Playback

1. Ensure you're in _NORMAL_ mode and then hit the `q` key to start macro recording
1. Next, Press a letter key `a-z`, the macro you're recording will be saved in this register (or "slot")
1. Perform editing operation as desired, all of this is being recorded into the macro. Press `q` again to stop recording
1. Replay the recorded macro by hitting the `@` key followed by the letter from step #2.
1. Macros can be composed like normal commands `10@a` will replay the macro in register `a` 10 times.
1. `@@` is handy to repeat the last macro (think `.` for the _WHOLE_ macro. `.` will only repeat the last command in the macro)

#### Saving Macros across Sessions

- vim automatically saves upto 50 lines of commands in each of the macro registers and restores them on editor restart
- users can explicitly set register contents via `vimrc` or the `^R^R` command 

Ref: `https://vim.fandom.com/wiki/Macros#Saving_a_macro` for more details

#### Dumping & Debugging Macros

vim macros cannot be debugged step-by-step (atleast as far as I'm aware) like debugging code with `gdb`. Here are a few handy pointers for checking macros and correcting any mistakes:

1. `:reg x` will print the contents of the register `x`, assuming macro was recorded here, it will display the recorded commands
1. `"xp` will "paste" the contents of register `x`, assuming macro was recorded here, you can have the contents pasted into the current buffer ("open file")
1. `"xyy` will "replace" the contents of register `x` with the line selected from the current buffer. This can be used to correct commands recorded wrongly in the macro

#### Notes/Links

Following are useful links for working with vim macros

```
https://vim.fandom.com/wiki/Macros
https://www.thegeekstuff.com/2009/01/vi-and-vim-macro-tutorial-how-to-record-and-play/
https://blog.sanctum.geek.nz/advanced-vim-macros/
https://math.berkeley.edu/~gbergman/misc/hacks/vi.html
https://unix.stackexchange.com/questions/17571/vim-markers-and-macros
```
