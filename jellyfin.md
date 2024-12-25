# Jellyfin 安装
`curl https://repo.jellyfin.org/install-debuntu.sh | sudo bash`

~~# Nvidia 显卡驱动安装
[ubuntu Docs](https://ubuntu.com/server/docs/nvidia-drivers-installation)~~

~~查看列表~~

~~`sudo ubuntu-drivers list`~~

~~安装驱动~~

~~`sudo ubuntu-drivers install ` or `sudo ubuntu-drivers install nvidia:550 `~~

~~安装NVENC/NVDEC~~

~~`sudo apt install -y libnvidia-decode libnvidia-encode` （需要选择对应驱动版本）~~

~~查看显卡信息~~

~~`nvidia-smi`~~

~~确认硬件解码正常~~

~~播放一个视频，并使用`nvidia-smi`查看。~~

# 安装QSV驱动

`sudo apt install -y intel-media-va-driver-non-free vainfo `

驱动安装完成后。进入`Jellyfin控制台->播放->转码->硬件加速`选择`Intel QuickSync(QSV)`，保存即可。

# Jellyfin 安装中文字体

`/usr/share/fonts/truetype/dejavu`目录中所有文件替换为有中文字体的字体文件，刷新元数据即可

# Jellyfin 字幕显示方框

服务器安装中文字体至`/usr/share/fonts`，进入`Jellyfin控制台->播放->转码`设置`备用字体路径`，勾选`启用备用字体`并`保存`




