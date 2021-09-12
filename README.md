# dotfiles

## `.vimrc` (neovim)

1. Install `neovim`: 
  ```bash
  sudo apt install neovim
  ```
2. Install [node.js](https://github.com/nodesource/distributions/blob/master/README.md):
  ```bash
  curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
  sudo apt-get install -y nodejs
  ```
3. Install [Pluggin Manager](https://github.com/junegunn/vim-plug)
  ```bash
  curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
  ```
4. Setup `init.vim`:
  ```bash
  mkdir ~/.config/nvim
  touch ~/.config/nvim/init.vim
  ```
5. Add to `init.vim` (insert the following in `init.vim`):
  ```vim
  set runtimepath^=~/.vim runtimepath+=~/.vim/after
  let &packpath=&runtimepath
  source ~/.vimrc
  ```
6. Edit `vimrc`
  Paste the vimrc from this repo into `~/.vimrc`
  
7. Install pluggins:
  Run `nvim`:
  ```bash
  nvim
  ```
  
  Run installer:
  ```vim
  :PlugInstall
  ```
