## 永久关闭无线网卡的 电源管理power management

Ubuntu 连接无线网wifi 容易断开 不稳定 完美解决

其中第二个步骤就是关闭power manager。百度上的方法基本上只给出了`sudo iwconfig wlp3s0 power off`这条命令，但是这只能临时生效，重启后就失效了。（wlp3s0是我的网卡名，你的不一定是这样）

最后谷歌中找到了方法。

## 查看电源管理

首先执行`sudo iwconfig`

```
enp0s25   no wireless extensions.

wlp3s0    IEEE 802.11  ESSID:"wonderful_world"  
          Mode:Managed  Frequency:2.462 GHz  Access Point: 8C:A6:DF:AE:E0:17   
          Bit Rate=121.5 Mb/s   Tx-Power=14 dBm   
          Retry short limit:7   RTS thr:off   Fragment thr:off
          Encryption key:off
          Power Management:on
          Link Quality=70/70  Signal level=-40 dBm  
          Rx invalid nwid:0  Rx invalid crypt:0  Rx invalid frag:0
          Tx excessive retries:115  Invalid misc:121   Missed beacon:0

lo        no wireless extensions.
```

从上面可以看到我的Power Management:on，也就是电源管理是开着的。

## 永久关闭

终端执行

```
sudo gedit /etc/NetworkManager/conf.d/default-wifi-powersave-on.conf
```

找到下面的
[connection]
wifi.powersave = 3
把3换成2并重新启动。

## 成功

然后运行`sudo iwconfig`，就能看到Power Management:off。