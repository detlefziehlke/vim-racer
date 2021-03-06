# Vim Racer Plugin

This plugin allows vim to use [Racer](http://github.com/phildawes/racer) for Rust code completion and navigation.

## Installation

1. Build / Install [Racer](http://github.com/phildawes/racer)

2. Install using Pathogen, Vundle or NeoBundle. Or, copy `plugin/racer.vim` into your `~/.vim/plugin` directory.

  Vundle users:
  ```
  Plugin 'racer-rust/vim-racer'
  ```

  NeoBundle users:
  ```
  NeoBundle 'racer-rust/vim-racer'
  ```
  
  vim-plug users:
  ```
  Plug 'racer-rust/vim-racer'
  ```
  
  Pathogen users:
  ```
  git clone --depth=1 https://github.com/racer-rust/vim-racer.git ~/.vim/bundle/vim-racer
  ```

3. Add `g:racer_cmd` to your `.vimrc`. Also it's worth turning on 'hidden' mode for buffers otherwise you need to save the current buffer every time you do a goto-definition. E.g.:

  ```
  set hidden
  let g:racer_cmd = "<path-to-racer>/target/release/racer"
  ```

4. If you want completions to show the complete function definition (e.g. its arguments and return type), enable the experimental completer:

  ```
  let g:racer_experimental_completer = 1
  ```

## Mappings

* In insert mode use `C-x-C-o` to search for completions

* In normal mode type `gd` to go to a definition

* In normal mode type `gs` to splitted open a definition

* In normal mode type `gx` to vsplitted open a definition
