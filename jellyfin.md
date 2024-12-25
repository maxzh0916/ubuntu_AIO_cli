# Jellyfin 安装
`curl https://repo.jellyfin.org/install-debuntu.sh | sudo bash`

# 安装QSV驱动

`sudo apt install -y intel-media-va-driver-non-free vainfo `

驱动安装完成后。进入`Jellyfin控制台->播放->转码->硬件加速`选择`Intel QuickSync(QSV)`，保存即可。

# Jellyfin 安装中文字体

`/usr/share/fonts/truetype/dejavu`目录中所有文件替换为有中文字体的字体文件，刷新元数据即可

# Jellyfin 字幕显示方框

服务器安装中文字体至`/usr/share/fonts`，进入`Jellyfin控制台->播放->转码`设置`备用字体路径`，勾选`启用备用字体`并`保存`
