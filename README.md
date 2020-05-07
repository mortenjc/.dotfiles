# My dotfiles

Based on https://medium.com/toutsbrasil/how-to-manage-your-dotfiles-with-git-f7aeed8adf8b

the files in $(HOME) can be added to the .dotfiles repo and thus be 1) reused
across hosts, 2) put under version control


## Initial setup
    > git init --bare $HOME/.dotfiles
    > alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
    > dotfiles config --local status.showUntrackedFiles no
    > dotfiles remote add origin git@github.com:mortenjc/.dotfiles.git

## Use
    > dotfiles status/add/commit/push
