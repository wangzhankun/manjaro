# change mirrors
<pre>
1.切换中国源
sudo vi /etc/pacman-mirrors.conf
如果提示没有gedit , 则执行命令 : sudo pacman -S gedit
或者干脆直接nano 编辑，默认是有的
修改如下地方为中国：
</pre>
<pre>
OnlyCountry = China
</pre>
<pre>
2.增加archlinuxcn软件仓库以及各种开发工具源

sudo vi /etc/pacman.conf

添加以下内容：
</pre>
<pre>

[archlinuxcn] 
SigLevel = Optional TrustedOnly 
Server = http://mirrors.ustc.edu.cn/archlinuxcn/$arch
Server= https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch
#both IPv4 &; IPv6 
#Server = https://mirrors.6.tuna.tsinghua.edu.cn/archlinuxcn/$arch 
# only IPv6#Server = https://mirrors.4.tuna.tsinghua.edu.cn/archlinuxcn/$arch 
# only IPv4#HTTP is also supported 
</pre>
<pre>
sudo pacman-mirrors -i -c China -m rank
sudo pacman-mirrors -g
sudo pacman -S archlinuxcn-keyring 
sudo pacman -Syyu 
</pre>
##  chang dirs into english
<pre>
vim .config/user-dirs.dirs
</pre>
# Install software
## vim
<pre>
sudo pacman -S vim
</pre>
## chrome
<pre>
sudo pacman -S google-chrome
</pre>
## Sougoupinyin
<pre>
sudo pacman -S fcitx-sogoupinyin
sudo pacman -S fcitx-im
sudo pacman -S fcitx-configtool
sudo gedit ~/.xprofile
        export GTK_IM_MODULE=fcitx
        export QT_IM_MODULE=fcitx
        export XMODIFIERS="@im=fcitx"
</pre>
## zsh & oh-my-zsh
<pre>
sudo pacman -S zsh zsh-completions
chsh -s /bin/zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
sudo pacman -S autojump
vim ~/.zshrc
        plugins=(git autojump)
</pre>
## uget & aria2
<pre>
sudo pacman -S uget
sudo pacman -S aria2
</pre>
## wechat
<pre>
sudo pacman -S electronic-wechat
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
