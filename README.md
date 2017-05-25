# FS-WR106

This is eventually going to be a repository of my personal LEDE builds for the FS-WR106.  For now it holds a stock 15.05 OpenWRT firmware.

The file *FS-WR106-stock-wrt-1505.zip* is a stock OpenWRT Chaos Carrier 15.05 build from the manufacturer.  They have not offered patches against stock 15.05 to date.

The stock firmware blob above is based on the OpenWRT WG3526 firmware build, but it holds the MAC address in another location.

The file *lede-ramips-mt7621-zbt-we1326-squashfs-sysupgrade.bin* is my build from LEDE master (r4188-e96a9a9af8) on 2017-05-25, with custom target, LuCI-ssl, and a few other changes inspired by @hnyman's WNDR builds.

# Partition Layout on FS-WR106 OEM build:

<pre>[    2.250000] Creating 4 MTD partitions on "spi32766.0":
[    2.260000] 0x000000000000-0x000000030000 : "u-boot"
[    2.260000] 0x000000030000-0x000000040000 : "u-boot-env"
[    2.270000] 0x000000040000-0x000000050000 : "factory"
[    2.270000] 0x000000050000-0x000002000000 : "firmware"
[    2.280000] mtd: partition "firmware" extends beyond the end of device "spi3
2766.0" -- size truncated to 0xfb0000
[    2.320000] 2 uimage-fw partitions found on MTD device firmware
[    2.330000] 0x000000050000-0x00000017e12e : "kernel"
[    2.330000] 0x00000017e12e-0x000001000000 : "rootfs"
[    2.340000] mtd: device 5 (rootfs) set to be root filesystem
[    2.340000] 1 squashfs-split partitions found on MTD device rootfs
[    2.350000] 0x0000006a0000-0x000001000000 : "rootfs_data"</pre>

