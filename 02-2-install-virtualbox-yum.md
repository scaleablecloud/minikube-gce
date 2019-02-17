Installing VirtualBox from Oracle repositories

* Start by downloading the build tools necessary for compiling the vboxdrv kernel module:
```
sudo yum -y install kernel-devel kernel-headers make patch gcc
 ```
 
* Download the Oracle Linux repo file to /etc/yum.repos.d directory using the following wget command:
``` 
sudo wget https://download.virtualbox.org/virtualbox/rpm/el/virtualbox.repo -P /etc/yum.repos.d
```

* Install the latest version of VirtualBox 5.2.x by typing

```
sudo yum -y install VirtualBox-5.2

```
* Verify that your VirtualBox installation

```
systemctl status vboxdrv
```

# Installing VirtualBox Extension Pack

* Download the extension pack file by typing:
```$xslt
wget https://download.virtualbox.org/virtualbox/5.2.20/Oracle_VM_VirtualBox_Extension_Pack-5.2.20.vbox-extpack
```

* import the extension pack
```$xslt
sudo VBoxManage extpack install  Oracle_VM_VirtualBox_Extension_Pack-5.2.20.vbox-extpack
```