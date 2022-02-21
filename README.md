Install latest neovim:
* sudo add-apt-repository ppa:neovim-ppa/unstable
* sudo apt update
* sudo apt install neovim
 
Install vim plug:
* From https://github.com/junegunn/vim-plug
* sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \ https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'

Create .config dir and create blank init.vim:
* mkdir -p ~/.config/nvim/
* touch ~/.config/nvim/init.vim
