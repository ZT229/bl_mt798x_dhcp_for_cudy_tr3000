# ATF and u-boot for mt798x with dhcpd

该项目不为您的机器负责，风险自担！
该项目不为您的机器负责，风险自担！
该项目不为您的机器负责，风险自担！

该项目源码基于如下源码移植

https://github.com/hanwckf/bl-mt798x.git

https://github.com/Yuzhii0718/bl-mt798x-dhcpd.git

## About bl-mt798x
- https://cmi.hanwckf.top/p/mt798x-uboot-usage

![](/u-boot.gif)

## Prepare

```
sudo apt install gcc-aarch64-linux-gnu build-essential flex bison libssl-dev device-tree-compiler qemu-user-static
```

## Build
```
无论何种分区布局都会默认生成atf（即bl2），该源码的bl2默认频率设定为1.6Ghz,根据自己机器的散热情况决定是否刷入


对于单分区布局（默认原厂分区布局即64M的ubi）
SOC=mt7981 BOARD=cudy_tr3000 MULTI_LAYOUT=0 ./build.sh
对于双分区布局
SOC=mt7981 BOARD=cudy_tr3000 MULTI_LAYOUT=1 ./build.sh
```
