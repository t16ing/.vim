.vim
===
     ____  __   _   ____  _  _  ___
    (_  _)/  ) / ) (_  _)( \( )/ __)
      )(   )( / _ \ _)(_  )  (( (_-.
     (__) (__)\___/(____)(_)\_)\___/'s vim configuration.


<!-- vim-markdown-toc GFM -->

* [What is `.vim`](#what-is-vim)
* [Sensible Configurations](#sensible-configurations)
* [Key Mappings](#key-mappings)
    * [Line, Buffer, Window, and Tab Motion](#line-buffer-window-and-tab-motion)
    * [Edit and Formatting](#edit-and-formatting)
    * [Selection](#selection)
    * [Marks and Register](#marks-and-register)
    * [File and Finder](#file-and-finder)
    * [Coding Navigation](#coding-navigation)
    * [Git Navigation](#git-navigation)
    * [Warning/Error Navigation](#warningerror-navigation)
    * [Integrated Development Environment](#integrated-development-environment)
    * [Markdown](#markdown)
    * [Spell](#spell)
    * [CoC List](#coc-list)
    * [Misc](#misc)
* [Commands](#commands)
* [Plugins](#plugins)
* [Support Languages](#support-languages)
* [Compatibility](#compatibility)
* [License](#license)

<!-- vim-markdown-toc -->

## What is `.vim`

This is my personal vim/neovim configurations.

It is designed as a sensible and powerful editor environment.

## Sensible Configurations

- Sensible motion, search, fold, and precede.
- More file format and encoding are supported.
- Persistent edit position and undo history. Auto read file changes from outside.
- Indent: 4 spaces, expand tabs. Highlight on tabs and unwanted spaces.
- Integrate with system clipboard.
- colorscheme: PaperColor Dark.

## Key Mappings

Use ',' as leader key.

Use ':' or ';' as command key.

### Line, Buffer, Window, and Tab Motion

Buffer and Line:

| Key                    | Action                                  |
|------------------------|-----------------------------------------|
| **`gj` `gk` `g<tab>`** | Next or previous or last opened buffer. |
| **`g<number>`**        | Goto buffer n.                          |
| **`<leader>bd`**       | Close buffer.                           |
| `W` `B`                | Faster word and back-word motion.       |
| `z.`                   | Put current line to center of screen.   |
| `z-`                   | Put current line to bottom of screen.   |

Window:

| Key                                          | Action                                                        |
|----------------------------------------------|---------------------------------------------------------------|
| **`<c-w>-` `<c-w>`<code>\ or &#124;</code>** | Split window.                                                 |
| **`<c-w>` then `j` or `k` or `h` or `l`**    | Move around in windows.                                       |
| `<c-w>` then `J` or `K` or `H` or `L`        | Move current window to topmost/bottommost/leftmost/rightmost. |
| `<c-w>_`                                     | Maximinze current window.                                     |
| `Q`                                          | Close current window.                                         |
| `q`                                          | Close a quick window.                                         |

Tab:

| Key        | Action                |
|------------|-----------------------|
| :tab split | Open new tab.         |
| :tabc      | Close current tab.    |
| :tabn      | Move to next tab.     |
| :tabp      | Move to previous tab. |

### Edit and Formatting

Coding style:

| Key                      | Action                               |
|--------------------------|--------------------------------------|
| **`>` and `<` and `==`** | Quick indent.                        |
| **(VISUAL)`=`**          | Selected range indent.               |
| `<leader>=`              | Format selected code.                |
| `<leader><leader>t`      | Expand tabs for buffer or selection. |

Code comment:

| Key    | Action                          |
|--------|---------------------------------|
| `gcc`  | Toggle comment.                 |
| `gcap` | Toggle comment for a paragraph. |

Clipboard:

| Key          | Action                   |
|--------------|--------------------------|
| `<leader>u`  | Open undo tree.          |
| `<leader>pp` | Toggle paste mode.       |
| `<a-p>`      | Cycle back yank history. |

### Selection

For searching:

| Key                          | Action                        |
|------------------------------|-------------------------------|
| **(VISUAL) then `*` or `#`** | Search for current selection. |
| **`<leader>/`**              | Disable highlight.            |

Surround editing:

| Key                   | Action                                         |
|-----------------------|------------------------------------------------|
| **`+` or `_`**        | Selection expanding or shrinking.              |
| `<c-s>`               | (coc) Language level selection expanding.      |
| **(VISUAL) then `S`** | Surround edit.                                 |
| **`cif` `vic`**       | `f` (function) and `c` (class) as text object. |

Multiple selection editing:

| Key                 | Action                                                                                 |
|---------------------|----------------------------------------------------------------------------------------|
| **`<c-n>`**         | Start multi-visual (EXTRA) mode: n confirm and q skip; `[ ]` for selection navigation. |
| *`<c-n>` then `\\a` | Visual multi selection and align.                                                      |
| `<c-n>` then `\\N`  | Visual multi selection and insert leading number.                                      |

### Marks and Register

Marks:

| Key              | Action                  |
|------------------|-------------------------|
| **`mm`**         | Toggle marks.           |
| **`mn` or `mp`** | Next or previous marks. |
| **`m<Space>`**   | Clear marks.            |
| **`ml`**         | Liast marks.            |

Register:

| Key                | Action                             |
|--------------------|------------------------------------|
| *`"` or `@`*       | Load from register.                |
| (INSERT)`<ctrl-r>` | Load from register in insert mode. |

### File and Finder

File manager:

| Key              | Action                          |
|------------------|---------------------------------|
| **`<leader>nn`** | Toggle nerdtree.                |
| **`<leader>nf`** | Open nerdtree in file location. |

Fuzzy finder:

| Key              | Action                              |
|------------------|-------------------------------------|
| **`<c-p>`**      | Fuzzy file finder.                  |
| **`<leader>ff`** | Search for the keyword.             |
| **`<leader>;`**  | Quick mapping for command history.  |
| **`<leader>/`**  | Search for searched patterns.       |
| **`<leader>fg`** | Git commits for the current buffer. |
| `<leader>fh`     | Search for the opened history.      |
| `<leader>ft`     | Search for global tags.             |
| `<leader>fl`     | Search for the lines.               |
| `<leader>fb`     | Search for opened buffer.           |

### Coding Navigation

| Key      | Action                 |
|----------|------------------------|
| **`tt`** | Toggle tagbar.         |
| **`gd`** | Go to definition.      |
| **`gf`** | Open file.             |
| `gy`     | Go to type definition. |
| `gi`     | Go to implementation.  |
| `gr`     | Go to references.      |

### Git Navigation

| Key              | Action              |
|------------------|---------------------|
| **`<leader>gb`** | Open git blame.     |
| **`<leader>gl`** | Open git log.       |
| `<leader>gt`     | Toggle git hunks.   |
| `]c` or `[c`     | Navigate git hunks. |

### Warning/Error Navigation

| Key          | Action                |
|--------------|-----------------------|
| `]e` or `[e` | Navigate lint errors. |
| `]g` or `[g` | Navigate diagnostics. |

### Integrated Development Environment

| Key                 | Action                                                      |
|---------------------|-------------------------------------------------------------|
| **(INSERT)`<tab>`** | Auto completion.                                            |
| **(INSERT)`<c-o>`** | Code Snippets.                                              |
| **`K`**             | Open document.                                              |
| `<leader>a`         | Apply code action, ex: `<leader>aap` for current paragraph. |
| `<leader>ac`        | Apply code action to current buffer.                        |
| `<leader>qf`        | Apply quick fix to the problem of the current line.         |
| `<leader>rn`        | Symbol rename.                                              |
| `<leader>R`         | Compile and Run.                                            |
| `<leader>T`         | Open terminal.                                              |

### Markdown

| Key                   | Action                      |
|-----------------------|-----------------------------|
| **`<leader>tm`**      | Toggle markdown table mode. |
| `<leader>tr`          | Format markdown table mode. |
| `<code>&#124;</code>` | Cell text object.           |

### Spell

| Key             | Action                         |
|-----------------|--------------------------------|
| **`<leader>ss`* | Toggle spell mode.             |
| **`<leader>sn`* | Next typo.                     |
| `<leader>sp`    | Previous typo.                 |
| **`<leader>sa`* | Add word to dict.              |
| `<leader>s?`    | Show all suggested correction. |
| **`<leader>sc`* | Apply spell correction         |
| **`<leader>cs`* | List suggested synonym.        |

### CoC List

| Key             | Action                                  |
|-----------------|-----------------------------------------|
| `<space>a`      | List CoC diagnostics.                   |
| `<space>e`      | List CoC extensions.                    |
| `<space>c`      | List CoC commands.                      |
| `<space>o`      | List CoC outlines.                      |
| `<space>s`      | List CoC symbols.                       |
| `<space>j or k` | Do default next or previous CoC action. |
| `<space>p`      | Resume previous CoC list.               |

### Misc

| Key               | Action                      |
|-------------------|-----------------------------|
| `zz`              | Save the file.              |
| `<leader>S`       | Open a fancy start screen.  |
| `<leader>rc`      | Open vimrc.                 |
| `<leader>rr`      | Reload vimrc.               |
| `<leader><space>` | Edit next placeholder <++>. |
| `tx`              | Place an AsciiArt.          |

## Commands

| Command    | Action                                                   |
|------------|----------------------------------------------------------|
| :SudoWrite | Write with sudo, requires ssh-askpass to input password. |
| :GenTocGFM | Generate markdown TOC for Github markdown.               |

## Plugins

Highlight:

- `vim-plug`: plugin manager.
- `nerdtree` family
    - `nerdtree-git-plugin`
    - `vim-nerdtree-syntax-highlight`
    - `vim-devicons`
- `lightline` family
    - `lightline-buffer`
    - `lightline-hunks`
    - `lightline-ale`
    - `vim-lightline-coc`
- `coc.nvim` extensions
    - `coc-json`
    - `coc-vimlsp`
    - `coc-phpls`
    - `coc-html`
    - `coc-css`
    - `coc-go`
    - `coc-tsserver`
    - `coc-pyright`
- auto completion, syntax highlight, linter checker, snippets
    - `tmux-completion`
    - `ale`
    - `ultisnips` and `vim-snippets`
- markdown family
    - `vim-instant-markdown`
    - `vim-table-mode`
    - `vim-markdown-toc`
- `fzf.vim` and `vim-rooter`

## Support Languages

- `Dockerfile`
- `python` (by `jedi.vim`)
- `c/c++`
- `php`
- `javascript`
- `typescript`
- `markdown`

## Compatibility

Below vim/neovim versions have been tested:

- NVIM v0.4.3
- Vim 8.1
- Vim 7.4

## License

MIT
