## Add basics from apt
```
sudo apt get wget curl git zsh -y
```

## Install micro:

```bash
curl https://getmic.ro | bash
sudo mv micro /usr/bin
micro -colorscheme dracula-tc
```

## Install EXA on ububuntu 20.04:

```bash
EXA_VERSION=$(curl -s "https://api.github.com/repos/ogham/exa/releases/latest" | grep -Po '"tag_name": "v\K[0-9.]+')
curl -Lo exa.zip "https://github.com/ogham/exa/releases/latest/download/exa-linux-x86_64-v${EXA_VERSION}.zip"
sudo unzip -q exa.zip bin/exa -d /usr/local
exa --version
rm -rf exa.zip
```

## Install oh-my-zsh

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Plugins:

#### zsh-autosuggestions

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
# plugins=(... zsh-autosuggestions)
```

#### zsh-syntax-highlighting

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
# plugins=( [plugins...] zsh-syntax-highlighting)
```

#### exa-zsh

```
git clone https://github.com/RitchieS/zsh-exa.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-exa
# plugins=(... zsh-exa)
```

#### powerlevel10k

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc
```
