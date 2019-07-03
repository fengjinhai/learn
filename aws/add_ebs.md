# 为EC2实例增加磁盘

参考：http://blog.51cto.com/beanxyz/1529931

* 查看加载的硬盘：`sudo fdisk -l`
* 格式化新硬盘：`sudo mkfs -t ext4 /dev/xvdf`
* 挂载新硬盘：`sudo mkdir /data && mount /dev/xvdf /data`
* 修改fstab文件：`sudo vim /etc/fstab`


# 为EC2卸载磁盘

* 卸载卷fastdfs: `umount -d /dev/xvdf`
* 删除/etc/fstab里面的uuid: `vim /etc/fstab/`
