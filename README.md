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
    * [Buffer, Window, and Tab Motion](#buffer-window-and-tab-motion)
    * [Edit and Formatting](#edit-and-formatting)
    * [Selection](#selection)
    * [Marks and Register](#marks-and-register)
    * [File Finder](#file-finder)
    * [Develop](#develop)
    * [Markdown](#markdown)
    * [Spell](#spell)
    * [CoC](#coc)
    * [Misc](#misc)
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

### Buffer, Window, and Tab Motion

| Key            | Action                   |
|----------------|--------------------------|
| Q              | Close window.            |
| <leader>bt     | Open buffer in new tab.  |
| <leader>bc     | Close tab.               |
| <leader>bd     | Close buffer.            |
| <c-w>- <c-w>\| | Split window.            |
| <shift-arrow>  | Window resize.           |
| bn, bp         | Next or previous buffer. |
| g<number>      | Goto buffer n.           |

### Edit and Formatting

| Key               | Action                               |
|-------------------|--------------------------------------|
| >, <, =           | Quick indent.                        |
| <leader>=         | Format selected code.                |
| <leader>tt        | Expand tabs for buffer or selection. |
| (visual)<enter>== | Quick alignment.                     |
| gcc               | Toggle comment.                      |
| gcap              | Toggle comment for a paragraph.      |
| <leader>u         | Open undo tree.                      |
| <leader>pp        | Toggle paste mode.                   |
| <leader>cc        | Toggle clean mode.                   |

### Selection

| Key                    | Action                                                         |
|------------------------|----------------------------------------------------------------|
| (visual)\*,#           | Search for current selection.                                  |
| <leader>/              | Disable highlight.                                             |
| W,B                    | Faster word and back-word motion.                              |
| <c-u>,<c-d>            | Scroll without moving cursor.                                  |
| <leader><leader>w or b | Easy move to word (forward or backward).                       |
| + or _                 | Expand or shrink selection.                                    |
| <c-n>                  | Start multi-visual mode, n for confirm and q for quick.        |
| f and c as text object | `cif` to change in function, `vic` to select whole class text. |
| <c-s>                  | Language level selection expanding.|

### Marks and Register

| Key               | Action                             |
|-------------------|------------------------------------|
| mm                | Toggle mark.                       |
| mn or mp          | Next or previous mark.             |
| m<number>         | Toggle marker.                     |
| mN or mP          | Next or previous marker.           |
| m<space> or m<BS> | Clear mark or marker.              |
| ml or mL          | Liast mark or marker.              |
| " or @            | Load from register.                |
| (insert)<ctrl-r>  | Load from register in insert mode. |

### File Finder

| Key        | Action                          |
|------------|---------------------------------|
| <leader>nn | Toggle nerdtree.                |
| <leader>nf | Open nerdtree in file location. |
| <c-p>      | Fuzzy find files.               |

### Develop

| Key            | Action                                                    |
|----------------|-----------------------------------------------------------|
| K              | Open document.                                            |
| tt             | Toggle tagbar.                                            |
| <leader>f      | Search for code.                                          |
| <c-j> or <c-k> | Navigate errors.                                          |
| gt             | Toggle git sign.                                          |
| gb             | Git blame.                                                |
| gl             | Git log.                                                  |
| ]c or [c       | Navigate hunks.                                           |
| gd             | Go to definition.                                         |
| gy             | Go to type definition.                                    |
| gi             | Go to implementation.                                     |
| gr             | Go to references.                                         |
| gf             | Open file.                                                |
| (insert)<c-o>  | Auto completion.                                          |
| ]g or [g       | Navigate diagnostics.                                     |
| <leader>a      | Apply code action, ex: <leader>aap for current paragraph. |
| <leader>ac     | Apply code action to current buffer.                      |
| <leader>qf     | Apply quick fix to the problem of the current line.       |
| <leader>rn     | Symbol rename.                                            |
| <leader>R      | Complie and Run.                                          |
| <leader>T      | Open terminal.                                            |

### Markdown

| Key        | Action                      |
|------------|-----------------------------|
| <leader>tm | Toggle markdown table mode. |
| <leader>tr | Format markdown table mode. |
| :GenTocGFM | Insert markdown TOC.        |

### Spell

| Key        | Action                         |
|------------|--------------------------------|
| <leader>ss | Toggle spell mode.             |
| <leader>sn | Next typo.                     |
| <leader>sp | Previous typo.                 |
| <leader>sa | Add word to dict.              |
| <leader>s? | Show all suggested correction. |
| <leader>sc | Apply spell correction         |
| <leader>cs | List suggested synonym.        |

### CoC

| Key           | Action                                  |
|---------------|-----------------------------------------|
| <space>a      | List CoC diagnostics.                   |
| <space>e      | List CoC extensions.                    |
| <space>c      | List CoC commands.                      |
| <space>o      | List CoC outlines.                      |
| <space>s      | List CoC symbols.                       |
| <space>j or k | Do default next or previous CoC action. |
| <space>p      | Resume previous CoC list.               |
| <leader>ne    | Open CoC file explorer.                 |

### Misc

| Key             | Action                     |
|-----------------|----------------------------|
| <leader>S       | Open a fancy start screen. |
| <leader>rc      | Open vimrc.                |
| <leader><space> | Edit next placeholder.     |
| tx              | Place an AsciiArt.         |

## Plugins

Highlight:

- `vim-plug`: plugin manager.
        Plug 'flazz/vim-colorschemes'
- `nerdtree`
    - `nerdtree-git-plugin`
    - `vim-nerdtree-syntax-highlight`
    - `vim-devicons`
- `lightline`:
    - `lightline#buffer`
    - `lightline#hunks`
    - `lightline#ale`
- `ctrlp.vim`
- `ack.vim`
- `ale`
- `jedi-vim`
- `coc.nvim`
- `tmux-completion`

For other plugins, please check out the `vimrc` [Plugins manager: vim-plug]() section.

## Supporting Languages

- Dockerfile
- `php`
- `python`
- `javascript`
- `typescript`
- `markdown`

## License

MIT
