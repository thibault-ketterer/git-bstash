# git-bstash
git branch stash

Are you annoyed by git stash being “per repository” only ?

# here is a git stash "by branch"

it saves your stash in a per branch file

# installation

if you don't have `~/bin`, create it

    mkdir -p ~/bin

download the file and chmod +x

    wget https://raw.githubusercontent.com/thibault-ketterer/git-bstash/refs/heads/main/git-bstash -O ~/bin/git-bstash
    chmod +x ~/bin/git-bstash

set your PATH if you don't have ~/bin in it

    echo "PATH=~/bin:$PATH" >> ~/.bashrc

zsh

    echo "PATH=~/bin:$PATH" >> ~/.zshrc

fish

    echo 'set -x PATH ~/bin $PATH' >> ~/.config/fish/config.fish

Then source your ~/.bashrc (or open a new terminal) and use the commands \o/

    git bstash save
    
    git bstash list
    
    git bstash show
    
/!\ it will destroy the stash

    git bstash drop

# add this to your fish prompt

    # branch stash
    if git bstash list
        set_color 96F
        echo -n "s⚑"
        set_color normal
    end
