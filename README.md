# init-macvlan

this scripts is testd in CentOS7 , kernel 3.10.0-862

# instasll

install `ifup-macvlan` , `ifdown-macvlan` scripts in `/etc/sysconfig/network-scripts` 


file `ifcfg-fake` is the configuration examples

```
#: macvlan 设备名称
#DEVICE=fake

#: 设备类型 表明是macvlan
#DEVICETYPE=macvlan

#: 用于 ip link
#TYPE=macvlan
#BOOTPROTO=none
#ONBOOT=yes
#NM_CONTROLLED=no

#： macvlan 绑定的父接口设备
#MACVLAN_PARENT=em2

#: macvlan 四种模式： private bridge vepa passthru
#MACVLAN_MODE=bridge

#: macvlan 设备配置的IP地址
#IPADDR=172.20.7.100

#: ip地址的子网掩码
#PREFIX=24

#: gateway
#GATEWAY=172.20.7.254
```

you must create macvlan config in `/etc/sysconfig/network-scripts` dir like `ifcfg-fake` file
