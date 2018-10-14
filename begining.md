# change mirrors
<pre>
sudo pacman-mirrors -gb testing -c China 
sudo pacman -S archlinuxcn -keyring 
sudo pacman -Syyu 
</pre>
##  chang dirs into english
<pre>
vim .config/user-dirs.dirspre
</pre>
# Install software
## vim
<pre>
sudo pacman -S vimpre
</pre>
## chrome
<pre>
sudo pacman -S google-chromepre
</pre>
## Sougoupinyin
<pre>
sudo pacman -S fcitxpre
sudo pacman -S fcitx-sogoupinyinpre
vim ~/.xprifilepre
        export GTK_IM_MODULE=fcitxpre
        export QT_IM_MODULE=fcitxpre
        export XMODIFIERS=@im=fcitxpre
</pre>
## zsh & oh-my-zsh
<pre>
sudo pacman -S zshpre
chsh -s /bin/zshpre
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"pre
sudo pacman -S autojumppre
vim ~/.zshrcpre
        plugins=(git autojump)pre
</pre>
## uget & aria2
<pre>
sudo pacman -S ugetpre
sudo pacman -S aria2pre
</pre>
## wechat
<pre>
sudo pacman -S electronic-wechatpre
</pre>
## zeal
<pre>
sudo pacman -S zeal
</pre>
and get docsets <a href = "https://github.com/Kapeli/feeds/">here</a>
## typora
<pre>
sudo pacman -S typora
</pre>
## vscode
