# dde-dock
Sometimes you will find your dde-dock & dde-launcher cannot open and find, you can try *downgrade deepin-daemon*.
# updating issue(gnome)
If you meet such a problem:<br/>
![problem](https://github.com/wangzhankun/manjaro/blob/master/pictures/undapte-issue.png?raw=true)
You may try the following
<pre>
sudo pacman -S manjaro-gnome-assets
sudo pacman -S manjaro-gnome-extension-settings-18.0
sudo pacman -Syyu
</pre>
# wps-sheet(gnome)
if you find some wrong color with yout wps , try the following
<pre>
sudo cp /bin/et /bin/et.bak
sudo vim /bin/et
</pre>
<pre>
${gInstallPath}/office6/${gApp} ${gOptExt} ${gOpt} "$@"
(maybe some difference)and change into
${gInstallPath}/office6/${gApp} -style motif ${gOptExt} ${gOpt} "$@"
</pre>
