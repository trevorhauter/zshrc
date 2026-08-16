# ZSH setup.

## Install ZSH
- https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH

## Install oh-my-zsh
```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install auto sugestions and syntax highlighting to oh-my-zsh
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

## Change your default shell (if not using zsh by default)
```sh
chsh -s $(which zsh)
```

## Clone this repo

I prefer to keep this repo in a `~/zshrc` directory

```sh
cd ~/ && git clone git@github.com:trevorhauter/zshrc.git
```

Remove the placeholder `~/.zshrc` file and simlink it to your new one

```sh
rm ~/.zshrc
ln -s ~/zshrc/.zshrc ~/.zshrc
```

## Working with local aliases or variables

If you wish to have aliases or environment variables that you want to keep out of version control, put them in a `.zshlocal` file in this directory. They will be included but ignored by VC.
