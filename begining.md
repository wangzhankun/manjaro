# change mirrors
<code>
sudo pacman-mirrors -gb testing -c China <br/>
sudo pacman -S archlinuxcn -keyring <br/>
sudo pacman -Syyu <br/>
</code> <br/>
# chang dirs into english
<code>
vim .config/user-dirs.dirs<br/>
</code>
# Install software
## vim
<code>
sudo pacman -S vim<br/>
</code>
## chrome
<code>
sudo pacman -S google-chrome<br/>
</code>
## Sougoupinyin
<code>
sudo pacman -S fcitx<br/>
sudo pacman -S fcitx-sogoupinyin<br/>
vim ~/.xprifile<br/>
        export GTK_IM_MODULE=fcitx<br/>
        export QT_IM_MODULE=fcitx<br/>
        export XMODIFIERS=@im=fcitx<br/>
</code>
## zsh & oh-my-zsh
<code>
sudo pacman -S zsh<br/>
chsh -s /bin/zsh<br/>
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"<br/>
sudo pacman -S autojump<br/>
vim ~/.zshrc<br/>
        plugins=(git autojump)<br/>
</code>
## uget & aria2
<code>
sudo pacman -S uget<br/>
sudo pacman -S aria2<br/>
</code>
## wechat
<code>
sudo pacman -S electronic-wechat<br/>
</code>

