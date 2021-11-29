删除桌面回收站图标

gsettings set org.gnome.shell.extensions.desktop-icons show-trash false

删除桌面用户文件夹图标

gsettings set org.gnome.shell.extensions.desktop-icons show-home false

ubuntu20.04 任务栏图标再次单击使打开的窗口最小化
在命令行运行如下命令：

1. 查看当前设置：

gsettings get org.gnome.shell.extensions.dash-to-dock click-action

默认是：‘focus-or-previews’。

2. 查看可设定值：

gsettings range org.gnome.shell.extensions.dash-to-dock click-action

可设定值如下：

enum
'skip'
'minimize'
'launch'
'cycle-windows'
'minimize-or-overview'
'previews'
'minimize-or-previews'
'focus-or-previews'
'quit'

3. 设置为'minimize-or-previews'，就可以实现再次单击使窗口最小化：

gsettings set org.gnome.shell.extensions.dash-to-dock click-action minimize-or-previews

//ALLEYLONE地址

85vepHig7BRFHPBELhcB8wD7M8MCgv5paWer9yjj4TcJA9jB2V8kBLPVuAS7JstngVfBSLWa9RDV2G8sGWX8ffuXSyHB7tw

//默认dz

461Mv9FHEVXR3Ht5daX2nJ6jQtuYiXnXmWsnZU1XVwmKcwMDivDijoNKNc87epPyZs92thDcN5AG3SC4scndkDKWMT4jG7v

//seed

同 亚 项 帮 术 柴 侦 汤 抗 库 猛 发 堂 底 艰 菜 玩 鲜 予 匀 株 福 数 接 接

