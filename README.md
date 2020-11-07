.vim
===
     ____  __   _   ____  _  _  ___
    (_  _)/  ) / ) (_  _)( \( )/ __)
      )(   )( / _ \ _)(_  )  (( (_-.
     (__) (__)\___/(____)(_)\_)\___/'s vim configuration.


<!-- vim-markdown-toc GFM -->

* [What is this for?](#what-is-this-for)
* [Sensible Configurations](#sensible-configurations)
* [Key Mappings](#key-mappings)
    * [Line, Buffer, Window, and Tab Motion](#line-buffer-window-and-tab-motion)
    * [Edit and Formatting](#edit-and-formatting)
    * [Selection](#selection)
    * [Marks and Register](#marks-and-register)
    * [File and Finder](#file-and-finder)
    * [Coding Navigation](#coding-navigation)
    * [Integrated Development Environment](#integrated-development-environment)
    * [Markdown](#markdown)
    * [Spell](#spell)
    * [CoC](#coc)
    * [Misc](#misc)
* [Commands](#commands)
* [Plugins](#plugins)
* [Supporting Languages](#supporting-languages)
* [License](#license)

<!-- vim-markdown-toc -->

## What is this for?

My personal vimrc configurations for vim/neovim.
Customization for sensible, comfortable, light and powerful editor environment.

## Sensible Configurations

- Sensible motion, search, fold, and precede.
- Wider file format and encoding support.
- Persistent edit position and undo history, and auto read file changes from outside.
- Indent: 4 spaces, expand tabs. Highlight for unwanted spaces.
- System clipboard integrated.
- colorscheme: PaperColor.

## Key Mappings

Use ',' as leader key.

### Line, Buffer, Window, and Tab Motion

| Key                      | Action                                   |
|--------------------------|------------------------------------------|
| `<leader>bt`             | Open buffer in new tab.                  |
| `<leader>bc`             | Close tab.                               |
| `<leader>bd`             | Close buffer.                            |
| `<c-w>-` `<c-w>\| or \\` | Split window.                            |
| `<shift-arrow>`          | Window resize.                           |
| `<c-w>_`                 | Maximinze current window.                |
| `gn` `gp` `g<tab>`       | Next or previous or last opened buffer.  |
| `g<number>`              | Goto buffer n.                           |
| `W` `B`                  | Faster word and back-word motion.        |
| `<c-u>` `<c-d>`          | Scroll without moving cursor.            |
| `<leader><leader>w or b` | Easy move to word (forward or backward). |

### Edit and Formatting

| Key                 | Action                               |
|---------------------|--------------------------------------|
| `> < =`             | Quick indent.                        |
| `<leader>=`         | Format selected code.                |
| `<leader>tt`        | Expand tabs for buffer or selection. |
| (VISUAL)`<enter>==` | Quick alignment.                     |
| `gcc`               | Toggle comment.                      |
| `gcap`              | Toggle comment for a paragraph.      |
| `<leader>u`         | Open undo tree.                      |
| `<leader>pp`        | Toggle paste mode.                   |

### Selection

| Key                      | Action                                                  |
|--------------------------|---------------------------------------------------------|
| (VISUAL)`* #`            | Search for current selection.                           |
| `<leader>/`              | Disable highlight.                                      |
| `+` or `_`               | Expand or shrink selection.                             |
| `<c-n>`                  | Start multi-visual mode, n for confirm and q for quick. |
| `cif` `vic`              | if (function) and ic (class) as text object.            |
| `<c-s>`                  | Language level selection expanding.                     |

### Marks and Register

| Key                   | Action                             |
|-----------------------|------------------------------------|
| `mm`                  | Toggle mark.                       |
| `mn` or `mp`          | Next or previous mark.             |
| `m<number>`           | Toggle marker.                     |
| `mN` or `mP`          | Next or previous marker.           |
| `m<space>` or `m<BS>` | Clear mark or marker.              |
| `ml` or `mL`          | Liast mark or marker.              |
| `"` or `@`            | Load from register.                |
| (INSERT)`<ctrl-r>`    | Load from register in insert mode. |

### File and Finder

| Key          | Action                             |
|--------------|------------------------------------|
| `<leader>nn` | Toggle nerdtree.                   |
| `<leader>nf` | Open nerdtree in file location.    |
| `<c-p>`      | Fuzzy file finder.                 |
| `<leader>ff` | Search for the keyword.            |
| `<leader>fh` | Search for the opened files.       |
| `<leader>ft` | Search for global tags.            |
| `<leader>fl` | Search for the lines.              |
| `<leader>fb` | Search for opened buffer.          |
| `<leader>f:` | Search for command history.        |
| `<leader>f/` | Search for searched patterns.      |
| `<leader>;`  | Quick mapping for command history. |

### Coding Navigation

| Key          | Action                 |
|--------------|------------------------|
| `tt`         | Toggle tagbar.         |
| `<leader>f`  | Search for code.       |
| `<leader>gb` | Open git blame.        |
| `<leader>gl` | Open git log.          |
| `<leader>gt` | Open git hunks.        |
| `]e` or `[e` | Navigate lint errors.  |
| `]c` or `[c` | Navigate git hunks.    |
| `gd`         | Go to definition.      |
| `gy`         | Go to type definition. |
| `gi`         | Go to implementation.  |
| `gr`         | Go to references.      |
| `gf`         | Open file.             |
| `]g` or `[g` | Navigate diagnostics.  |

### Integrated Development Environment

| Key             | Action                                                      |
|-----------------|-------------------------------------------------------------|
| (INSERT)`<c-o>` | Auto completion.                                            |
| `K`             | Open document.                                              |
| `<leader>a`     | Apply code action, ex: `<leader>aap` for current paragraph. |
| `<leader>ac`    | Apply code action to current buffer.                        |
| `<leader>qf`    | Apply quick fix to the problem of the current line.         |
| `<leader>rn`    | Symbol rename.                                              |
| `<leader>f`     | Show name usages.                                           |
| `<leader>R`     | Complie and Run.                                            |
| `<leader>T`     | Open terminal.                                              |

### Markdown

| Key          | Action                      |
|--------------|-----------------------------|
| `<leader>tm` | Toggle markdown table mode. |
| `<leader>tr` | Format markdown table mode. |
| `:GenTocGFM` | Insert markdown TOC.        |

### Spell

| Key          | Action                         |
|--------------|--------------------------------|
| `<leader>ss` | Toggle spell mode.             |
| `<leader>sn` | Next typo.                     |
| `<leader>sp` | Previous typo.                 |
| `<leader>sa` | Add word to dict.              |
| `<leader>s?` | Show all suggested correction. |
| `<leader>sc` | Apply spell correction         |
| `<leader>cs` | List suggested synonym.        |

### CoC

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

| Key               | Action                        |
|-------------------|-------------------------------|
| `Q`               | Close window.                 |
| `S`               | Write buffer to current file. |
| `<leader>S`       | Open a fancy start screen.    |
| `<leader>rc`      | Open vimrc.                   |
| `<leader>rr`      | Reload vimrc.                 |
| `<leader><space>` | Edit next placeholder.        |
| `tx`              | Place an AsciiArt.            |

## Commands

| Command    | Action                                                   |
|------------|----------------------------------------------------------|
| :SudoWrite | Write with sudo, requires ssh-askpass to input password. |
| :GenTocGFM | Generate markdown TOC for Github markdown.               |

## Plugins

Highlight:

- `vim-plug`: plugin manager.
        Plug 'flazz/vim-colorschemes'
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
- auto completion, syntax highlight, and linter checker
    - `tmux-completion`
    - `ale`
    - `jedi-vim`
- `fzf.vim`

For other plugins, please check out the `vimrc` [Plugins manager: vim-plug]() section.

## Supporting Languages

- Dockerfile
- `python` (by `jedi.vim`)
- `php`
- `javascript`
- `typescript`
- `markdown`

## License

MIT
