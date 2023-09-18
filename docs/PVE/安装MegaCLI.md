# 安装MegaCLI

## 安装依赖

```
# zip
apt-get install zip -y
# alien
apt-get install alien -y
# libncurses5 https://gist.github.com/metajiji/cf859a7fc65a63690ecb208d11ea8407?permalink_comment_id=4469291#gistcomment-4469291
apt-get install libncurses5
```

## 下载安装

```
curl -LO https://docs.broadcom.com/docs-and-downloads/raid-controllers/raid-controllers-common-files/8-07-14_MegaCLI.zip
unzip 8-07-14_MegaCLI.zip
cd Linux
sudo alien MegaCli-8.07.14-1.noarch.rpm  # convert from rpm to deb first
sudo dpkg -imegacli_8.07.14-2_all.deb
```

## 快捷方式

```
sudo update-alternatives --install '/usr/bin/MegaCli64' 'MegaCli64' '/opt/MegaRAID/MegaCli/MegaCli64' 1
sudo update-alternatives --install '/usr/bin/MegaCli' 'MegaCli' '/opt/MegaRAID/MegaCli/MegaCli64' 1
sudo update-alternatives --install '/usr/bin/megacli' 'megacli' '/opt/MegaRAID/MegaCli/MegaCli64' 1
```

## 参考资料

https://gist.github.com/metajiji/cf859a7fc65a63690ecb208d11ea8407