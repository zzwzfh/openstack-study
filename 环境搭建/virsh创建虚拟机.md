#virsh创建虚拟机
- 使用iso镜像装系统
1. virsh-install 
	```bash
	virt-install  --name=centos-basic --ram 512 --vcpus=2 --arch=x86_64 --os-type=linux --disk path=/home/ubuntu/centos-basic.qcow2,device=disk,bus=virtio,format=qcow2 --accelerate --cdrom /home/ubuntu/CentOS-7-x86_64-DVD-1511.iso --graphics vnc --network bridge=br0 --force --autostart
	```

2. 使用vnc连接装系统
遇到问题，连接后闪退
>**solved:** 依次点Option-->Advanced-->Expert找到ColourLevel，默认值是pal8，修改为rgb222或full。

3. 接下来是正常装系统过程


- 使用已经装好系统的镜像