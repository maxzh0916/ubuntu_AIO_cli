# mdadm
组建软磁盘阵列

## 查看可用磁盘
`sudo lsblk`

## 创建RAID
`sudo mdadm --create --verbose /dev/md0 --level=0 --raid-devices=2 /dev/sda /dev/sdb`

## 格式化RAID
`sudo mkfs.ext4 /dev/md0`

## 查看uuid
`sudo blkid /dev/md0`

## 自动挂载
`sudo nano /etc/fstab`最后添加`/dev/disk/by-uuid/uuid /挂载点 ext4 defaults 0 2`

## 保存配置
`sudo update-initramfs -u`
`sudo mdadm --detail --scan`
