# material.vim

A port of the [Material](https://material-theme.site) color scheme for Vim/Neovim,
with a few customizations.

## Installation

Using [vim-plug](https://github.com/junegunn/vim-plug) (modify this to work with your Vim package manager of choice):

For the original version:
```vim
Plug 'kaicataldo/material.vim'
```
For my own version:
```vim
Plug 'grussorusso/material.vim', {'branch': 'main'}
```

## Usage

To enable this color scheme, add the following to your Vim (`~/.vimrc`) or Neovim (`~/.config/nvim/init.vim`) configuration:

```vim
colorscheme material
```

### True Colors

True colors are a requirement for this color scheme to work properly. To enable this, place the following in your `~/.vimrc` or `~/.config/nvim/init.vim` file:

```vim
" For Neovim 0.1.3 and 0.1.4 - https://github.com/neovim/neovim/pull/2198
if (has('nvim'))
  let $NVIM_TUI_ENABLE_TRUE_COLOR = 1
endif

" For Neovim > 0.1.5 and Vim > patch 7.4.1799 - https://github.com/vim/vim/commit/61be73bb0f965a895bfb064ea3e55476ac175162
" Based on Vim patch 7.4.1770 (`guicolors` option) - https://github.com/vim/vim/commit/8a633e3427b47286869aa4b96f2bfc1fe65b25cd
" https://github.com/neovim/neovim/wiki/Following-HEAD#20160511
if (has('termguicolors'))
  set termguicolors
endif
```

### Theme

There are five theme options - `default`, `palenight`, `ocean`, `lighter`, and `darker` (defaulting to `default`). This can be configured as follows:

```vim
let g:material_theme_style = 'default' | 'palenight' | 'ocean' | 'lighter' | 'darker'
```

### Italics

To enable italics (`0` or off by default), please add the following to your configuration file:

```vim
let g:material_terminal_italics = 1
```

### Full configuration example

```vim
let g:material_terminal_italics = 1
let g:material_theme_style = 'lighter'
colorscheme material
```

### lightline.vim

To use the theme, install [lightline.vim](https://github.com/itchyny/lightline.vim) with your Vim package manager of choice and then add the following to your configuration file:

```vim
let g:lightline = { 'colorscheme': 'material_vim' }
```

The theme will change to match the theme option specified.


To use the included [vim-airline](https://github.com/vim-airline/vim-airline) theme:

```vim
let g:airline_theme = 'material'
```

### Terminal Color Scheme

Corresponding terminal color schemes are included in this repo. You can find them [here](https://github.com/kaicataldo/material.vim/tree/master/terminal-colors/).


## Thanks

Thanks to [@equinusocio](https://github.com/equinusocio) for the original Material theme as well as [palenight.vim](https://github.com/drewtempelmeyer/palenight.vim) and [quantum](https://github.com/tyrannicaltoucan/vim-quantum), both of which were of great help when I first started this project.
