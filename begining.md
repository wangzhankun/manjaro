# Change mirrors

<pre>
sudo pacman-mirrors -i -c China -m rank
sudo pacman -Syyu 
</pre>

##  chang dirs into english
<pre>
vim .config/user-dirs.dirs
</pre>
# Beauty

```bash
sudo pacman -S yaourt
yaourt electron-ssr
yaourt numix-gtk-theme
yaourt numix-circle-icon-theme-git
sudo pacman -S docky
```

And then, search *sweet* in https://www.gnome-look.org/

Download and install it with the help of instruction.

Change it by gnome-tweak.



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

		export LANG=zh_CN.UTF-8
		export LANGUAGE=zh_CN:en_US
		export LC_CTYPE=en_US.UTF-8
		
		export XIM=fctix
		export XIM_PROGRAM=fctix
	    export GTK_IM_MODULE=fcitx
	    export QT_IM_MODULE=fcitx
	    export XMODIFIERS="@im=fcitx"
</pre>

## zsh & oh-my-zsh
<pre>
sudo pacman -S zsh zsh-completions curl
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
<pre>
sudo pacman -S visual-studio-code-bin
</pre>
