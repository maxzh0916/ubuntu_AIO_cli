# hdparm

硬盘休眠设置

# 安装

`$ sudo apt-get install hdparm `

# 检查硬盘设备

`$ lsblk`

# 查看硬盘状态

`$ sudo hdparm -C /dev/sdb`

休眠：`standby`
运行：`active` & `idle`

# 设置休眠时间

编辑

`$ sudo nano /etc/hdparm.conf`
在最后添加

```
/dev/sdb {
    force_spindown_time = 36
}
```

执行使休眠生效

`sudo /usr/lib/pm-utils/power.d/95hdparm-apm resume`
