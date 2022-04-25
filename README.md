Before installing Neovim + CoC plugins you'll want to install the latest versions of node (from PPA) + rust:

Node
* curl -sL https://deb.nodesource.com/setup_16.x -o /tmp/nodesource_setup.sh
* sudo bash /tmp/nodesource_setup.sh
* sudo apt install nodejs
* node --version

Rust (WSL specific, see: https://www.rust-lang.org/tools/install).
Default installation is fine. CoC will install dependencies for rust-analyzer.
* curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

Install latest neovim:
* sudo add-apt-repository ppa:neovim-ppa/unstable
* sudo apt update
* sudo apt install neovim
* alias vim="nvim"
 
Install vim plug:
* From https://github.com/junegunn/vim-plug
* sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'

Get init.vim and place it where it's expected:
* mkdir -p ~/.config/nvim/
* git clone https://github.com/MichaelBrown08/myNvimrc
* mv myNvimrc/init.vim .config/nvim/

In Neovim run:
* :CocInstall coc-tsserver coc-json coc-rust-analyzer
* When you first open a rust directory (create one with `cargo new <name>`) in nvim it'll ask you to accept an installation
