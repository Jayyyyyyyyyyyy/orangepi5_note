# 方法一 使用RKDevTool烧录系统镜像到TF卡
环境windows，参考orangepi5手册第28页

# 方法二 基于Ubuntu将系统镜像烧写到TF卡
环境Ubuntu，参考orangepi5手册第38页

## 镜像：Orange Pi OS (Arch)
http://www.orangepi.cn/html/hardWare/computerAndMicrocontrollers/service-and-support/Orange-pi-5.html

## 开机创建用户和密码，完成配置重启
- 使用ssh连接，先查看ip地址
- 客户端使用ssh-keygen -R <ip> 更新远程秘钥
- ssh远程登录
- 更新系统包数据库sudo pacman -Sy
- 安装mosh sudo pacman -S mosh
- shell 美化curl -s https://ohmyposh.dev/install.sh | bash -s
- echo 'export PATH=$PATH:$HOME/.local/bin' >> ~/.bashrc
- source ~/.bashrc

# 2. 安装 mosh
sudo pacman -S mosh

# mipi摄像头调试
参考orangepi5手册第467页
sudo vim /boot/extlinux/extlinux.conf 
添加此配置： Cam3接 ov13850
FDTOVERLAYS /dtbs/rockchip/overlay/rk3588-ov13850-c3.dtbo



