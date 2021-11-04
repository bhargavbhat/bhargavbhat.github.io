Title: Intro to vim - Session 1 Notes
Date: 2012-08-15 09:17
Category: tools
Tags: vim, editor
Authors: Bhargav Bhat
Summary: Notes from 1st Session of introduction to vim

_This is a collection of notes and paraphrasing of Q&A from the 3 sessions of approx 45mins each. These sessions covered the basics of vim, presented over the last few weeks to team members and other interested colleagues. The focus of these sessions was more on improving day to day work efficiency with vim_

#### Introduction
vim is an open-source, multi-platform text editor with various advanced features. The main selling point of vim is that once you've learnt the editor and its various modes, options and commands, you can use it to process all kinds of text files, not just code & configuration. Many people use vim to write/edit email and documents also. vim is extensible and can be configured to help with text editing tasks of all sorts of things. eg: documentation in markdown (with shortcut for previewing in browser), plugin for plantUML previews and similar.

#### Installation
vim can be installed via PeaCy on Windows or with `apt-get` on Ubuntu. The low-foot print simulator images and build servers have `vi` which is a lesser featured cousin of vim already for quick editing tasks such as tweaking config files and such.

#### Customization
vim can be customized via the `vimrc` file, which determines the behaviour of the editor, the syntax highlighting and plugins available as well as general features such as keyboard-shortcuts (which vim names as keybindings). vim is extermely customizable and it wouldn't be possible to cover all the options and settings available in this session. Refer to links below for a sample vimrc which will serve as a good starting point as well as suggestions for customizing the editor

```
https://vim.fandom.com/wiki/Example_vimrc
https://nvie.com/posts/how-i-boosted-my-vim/
https://developer.ibm.com/tutorials/au-customize_vi/
```

*Note:* We will revisit customization in later sessions, so for now, this section can be skimmed to get an idea of the vast options available for adjusting the behaviour of the editor itself

#### Differences & Key Concepts
vim feels a little different from most other editors such as say `Notepad++` or `nano` due to the different philosophy that vim employs to deal with editing. Below are the key points of the vim philosophy, as per my understanding:

- *Modality* - Separates editing/reading (_NORMAL_ mode) text from inputing/writing text (_INSERT_ mode). This allows effectively supercharges the two below principles.
- *Orthogonality* - Separates the notion of movement/selection from actions/changes. This allows the user to determine the region or items to change independent of the change itself
- *Composability* - Allows "building" up of changes from primitives that the user is already familiar with, these can further be built into macros for effective processing of repeitive tasks

Of course, this is a personal view/opinion and various people would have a different view on these aspects.

#### Basic Commands
Keeping with the philosophy of Orthogonality & Composability, vim commands can be divided into two groups as below:


| Movements   | Actions     |
| ----------- | ----------- |
| `0` start of line  | `d` delete |
| `$` end of line    | `c` change |
| `w` next word      | `y` yank (remember as cop*y*) |
| `b` previous word  | `.` repeat prev action |


These commands can then be combined to express the editing the user wants to perform. Eg: `d$` will delete the current line (compare this with say Notepad++, where user needs to select the entire line with mouse and hit delete/backspace). A lot of the power of vim comes from these commands. Please refer to the links below that go into a lot more detail on vim commands (basic and intermediate):

```
https://vim.fandom.com/wiki/Tutorial
https://www.linux.com/training-tutorials/vim-101-beginners-guide-vim/
https://stackoverflow.com/questions/1276403/simple-vim-commands-you-wish-youd-known-earlier/1278813
https://thoughtbot.com/upcase/vim
https://code.tutsplus.com/articles/25-vim-tutorials-screencasts-and-resources--net-14631
```

We would cover language specific features and advanced concepts such as macros in the upcoming sessions, as well as how it applies specifically to the day to day tasks that we spend a lot of time on:
- rationalizing logs from devices/field
- narrowing down relevant parts of the logs with custom folds
- macros to "boil down" log file and list out relevant/interesting lines from point of view of reproducing the bug and/or capturing state


*Migration Notes:* Q&A Part not captured as I couldn't find those paper notes, the original post had a `TODO` with typing out Q&A questions into blogger post. Sessions 2 & 3 were focussed on practical examples relevant to the team that I was then a part of and therefore have not been migrated.

