# change mirrors
<pre>
1.切换中国源
sudo gedit /etc/pacman-mirrors.conf
如果提示没有gedit , 则执行命令 : sudo pacman -S gedit
或者干脆直接nano 编辑，默认是有的
修改如下地方为中国：
</pre>
<pre>
OnlyCountry = China
</pre>
<pre>
2.增加archlinuxcn软件仓库以及各种开发工具源

sudo gedit /etc/pacman.conf

添加以下内容：
</pre>
<pre>


[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = http://mirrors.ustc.edu.cn/archlinuxcn/$arch

[arch4edu]
SigLevel = Never
Server = http://mirrors.tuna.tsinghua.edu.cn/arch4edu/$arch

</pre>
<pre>
sudo pacman-mirrors -i -c China -m rank
sudo pacman-mirrors -g
sudo pacman -S archlinuxcn-keyring 
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
