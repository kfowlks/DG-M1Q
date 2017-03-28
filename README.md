# DG-M1Q
DG-M1Q 2017 Smart Home 960P 2.8mm

Notes:


Firmware: - 22.0.0.12
```
Initial Firmware
Starting Nmap 7.01 ( https://nmap.org ) at 2017-03-28 18:23 EDT
Nmap scan report for 192.168.1.13
Host is up (0.0096s latency).
Not shown: 998 closed ports
PORT     STATE SERVICE
554/tcp  open  rtsp
5000/tcp open  upnp
```

Firmware: - 22.0.0.16
```
Starting Nmap 7.01 ( https://nmap.org ) at 2017-03-28 18:23 EDT
Nmap scan report for 192.168.1.13
Host is up (0.0088s latency).
Not shown: 997 closed ports
PORT     STATE SERVICE
23/tcp   open  telnet
554/tcp  open  rtsp
5000/tcp open  upnp
```
```
telnet 192.168.1.13
```
goke login: root

NO PASSWORD

dmesg

```
# dmesg 
[    0.000000] Booting Linux on physical CPU 0
[    0.000000] Linux version 3.4.43-gk (user15@ubuntu) (gcc version 4.6.1 (crosstool-NG 1.18.0) ) #56 PREEMPT Fri Sep 29 00:24:56 PDT 2006
[    0.000000] CPU: ARMv6-compatible processor [410fb767] revision 7 (ARMv7), cr=00c5387d
[    0.000000] CPU: VIPT aliasing data cache, VIPT aliasing instruction cache
[    0.000000] Machine: Goke GK7102 RB_JXH42 board V2.00
[    0.000000] Memory policy: ECC disabled, Data cache writeback
[    0.000000] AHB: 0x90000000  0xf2000000  -- 0x1000000
[    0.000000] APB: 0xa0000000  0xf3000000  -- 0x1000000
[    0.000000] PPM: 0xc0000000  0xc0000000  -- 0x200000
[    0.000000] BSB: 0xc2500000  0xf5000000  -- 0x200000
[    0.000000] DSP: 0xc2700000  0xf6000000  -- 0x1900000
[    0.000000] hal version = 20151223 
[    0.000000] On node 0 totalpages: 8960
[    0.000000] free_area_init_node: node 0, pgdat 8045c430, node_mem_map 80493000
[    0.000000]   Normal zone: 70 pages used for memmap
[    0.000000]   Normal zone: 0 pages reserved
[    0.000000]   Normal zone: 8890 pages, LIFO batch:1
[    0.000000] pcpu-alloc: s0 r0 d32768 u32768 alloc=1*32768
[    0.000000] pcpu-alloc: [0] 0 
[    0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 8890
[    0.000000] Kernel command line: console=ttySGK0,115200 noinitrd mem=35M rw mtdparts=gk7101_flash:256K(boot),64K(bootenv),2560K(kernel),7168K(rootfs),1024K(rom),5312K(APP) rootfstype=squashfs root=/dev/mtdblock3 init=linuxrc ip=192.168.1.229:192.168.1.225:192.168.1.1:255.255.255.0:"gk7101":eth0 mac=3C:97:0E:22:E1:14 phytype=0
[    0.000000] PID hash table entries: 256 (order: -2, 1024 bytes)
[    0.000000] Dentry cache hash table entries: 8192 (order: 3, 32768 bytes)
[    0.000000] Inode-cache hash table entries: 4096 (order: 2, 16384 bytes)
[    0.000000] Memory: 35MB = 35MB total
[    0.000000] Memory: 30760k/30760k available, 5080k reserved, 0K highmem
[    0.000000] Virtual kernel memory layout:
[    0.000000]     vector  : 0xffff0000 - 0xffff1000   (   4 kB)
[    0.000000]     fixmap  : 0xfff00000 - 0xfffe0000   ( 896 kB)
[    0.000000]     DMA     : 0xff600000 - 0xffe00000   (   8 MB)
[    0.000000]     vmalloc : 0x82800000 - 0xff000000   (1992 MB)
[    0.000000]     lowmem  : 0x80000000 - 0x82300000   (  35 MB)
[    0.000000]     modules : 0x7f000000 - 0x80000000   (  16 MB)
[    0.000000]       .text : 0x80008000 - 0x80413000   (4140 kB)
[    0.000000]       .init : 0x80413000 - 0x80433000   ( 128 kB)
[    0.000000]       .data : 0x80434000 - 0x8045cd00   ( 164 kB)
[    0.000000]        .bss : 0x8045cd24 - 0x8048edf8   ( 201 kB)
[    0.000000] NR_IRQS:128
[    0.000000] >> gk7101 init irq vic1...
[    0.000000] >> gk7101 init irq vic2...
[    0.000000] gk7101 init vic...
[    0.000000] mach gk7101 init timer...
[    0.000000] sched_clock: 32 bits at 100 Hz, resolution 10000000ns, wraps every 4294967286ms
[    0.000000] Console: colour dummy device 80x30
[    0.000000] console [ttySGK0] enabled
[    0.010000] Calibrating delay loop... 597.60 BogoMIPS (lpj=2988032)
[    0.070000] pid_max: default: 32768 minimum: 301
[    0.070000] Mount-cache hash table entries: 512
[    0.080000] CPU: Testing write buffer coherency: ok
[    0.090000] Setting up static identity map for 0xc0542e30 - 0xc0542e68
[    0.100000] NET: Registered protocol family 16
[    0.110000] gk7101 init timer...
[    0.110000] Init HW timer for DSP communication
[    0.120000] gk7101 init gpio...
[    0.120000] gpiochip_add: registered GPIOs 0 to 63 on device: gk7101-gpio0
[    0.130000] gpio map init...
[    0.130000] create proc dir
[    0.140000] gk7101 register devices 8
[    0.140000] gk7101 register I2C
[    0.280000] bio: create slab <bio-0> at 0
[    0.290000] spi spi.0: gk7101 SPI Controller 0 created 
[    0.290000] spi spi.0: master is unqueued, this is deprecated
[    0.300000] usbcore: registered new interface driver usbfs
[    0.310000] usbcore: registered new interface driver hub
[    0.310000] usbcore: registered new device driver usb
[    0.320000] i2c regbase: 0xf3003000 
[    0.320000] i2c i2c.0: i2c irq:registers 9
[    0.330000] i2c i2c.0: GK7101 I2C[0] adapter[i2c-0] probed!
[    0.340000] FS-Cache: Loaded
[    0.340000] CacheFiles: Loaded
[    0.350000] cfg80211: Calling CRDA to update world regulatory domain
[    0.360000] gk7101-sd gk7101-sd.0: Slot0 req_size=0x00010000, segs=16, seg_size=0x00010000
[    0.390000] gk7101-sd gk7101-sd.0: GK7101 SD/MMC[0] has 1 slots @ 46000000Hz, [0x09e130b0:0x00000000]
[    0.400000] NET: Registered protocol family 2
[    0.400000] IP route cache hash table entries: 1024 (order: 0, 4096 bytes)
[    0.410000] TCP established hash table entries: 2048 (order: 2, 16384 bytes)
[    0.420000] TCP bind hash table entries: 2048 (order: 1, 8192 bytes)
[    0.430000] TCP: Hash tables configured (established 2048 bind 2048)
[    0.440000] TCP: reno registered
[    0.440000] UDP hash table entries: 256 (order: 0, 4096 bytes)
[    0.450000] UDP-Lite hash table entries: 256 (order: 0, 4096 bytes)
[    0.450000] NET: Registered protocol family 1
[    0.460000] RPC: Registered named UNIX socket transport module.
[    0.470000] RPC: Registered udp transport module.
[    0.470000] RPC: Registered tcp transport module.
[    0.480000] RPC: Registered tcp NFSv4.1 backchannel transport module.
[    0.480000] mdma init...
[    0.490000] mdma request irq: 54 
[    0.500000] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.500000] NFS: Registering the id_resolver key type
[    0.510000] jffs2: version 2.2. (NAND) © 2001-2006 Red Hat, Inc.
[    0.520000] msgmni has been set to 60
[    0.530000] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 253)
[    0.540000] io scheduler noop registered
[    0.540000] io scheduler deadline registered
[    0.550000] io scheduler cfq registered (default)
[    0.550000] Serial: gk7101_uart driver
[    0.550000] serial_gk7101_probe: entry
[    0.550000] uart.0: ttySGK0 at MMIO 0xa0005000 (irq = 31) is a gk7101uart
[    0.560000] serial_gk7101_probe: succeed!
[    0.560000] serial_gk7101_probe: entry
[    0.560000] uart.1: ttySGK1 at MMIO 0xa001f000 (irq = 15) is a gk7101uart
[    0.570000] serial_gk7101_probe: succeed!
[    0.570000] serial_gk7101_probe: entry
[    0.570000] uart.2: ttySGK2 at MMIO 0xa001e000 (irq = 27) is a gk7101uart
[    0.580000] serial_gk7101_probe: succeed!
[    0.590000] brd: module loaded
[    0.590000] loop: module loaded
[    0.600000] adc initialized (10:11)
[    0.600000] slram: not enough parameters.
[    0.610000] speed_mod is 0
[    0.610000] support 4X mode read:0xe520f1ff
[    0.620000] gk7101_flash gk7101_flash.0: MX25L12845 (16384 Kbytes)
[    0.620000] 6 cmdlinepart partitions found on MTD device gk7101_flash
[    0.630000] Creating 6 MTD partitions on "gk7101_flash":
[    0.640000] 0x000000000000-0x000000040000 : "boot"
[    0.640000] 0x000000040000-0x000000050000 : "bootenv"
[    0.650000] 0x000000050000-0x0000002d0000 : "kernel"
[    0.660000] 0x0000002d0000-0x0000009d0000 : "rootfs"
[    0.660000] 0x0000009d0000-0x000000ad0000 : "rom"
[    0.670000] 0x000000ad0000-0x000001000000 : "APP"
[    0.680000] GKETH_init
[    0.680000] [GKETH_drv_probe] eth_base = 0xf200e000
[    0.690000] mii id = 0 
[    0.690000] ###### PHY Reset.1.0.2
[    0.810000] mdiobus_register: PHY[0] whose id 0x00000000 
[    0.810000] goke MII Bus: probed
[    0.820000] gk7101-eth gk7101-eth.0: MAC Address[3e:97:0e:22:e1:14].
[    0.830000] usbcore: registered new interface driver cdc_wdm
[    0.830000] usbcore: registered new interface driver libusual
[    0.840000] musb-hdrc: version 6.0, ?dma?, otg (peripheral+host)
[    0.850000] musb phy Begin initial sequence ...
[    1.090000] gk7101 musb init end...
[    1.100000] musb-hdrc: ConfigData=0x03 (UTMI-16, SoftConn)
[    1.100000] musb-hdrc: MHDRC RTL version 2.0 
[    1.100000] musb-hdrc musb-hdrc: MUSB HDRC host driver
[    1.100000] musb-hdrc musb-hdrc: new USB bus registered, assigned bus number 1
[    1.110000] vm : ffde0000, phy : c21a0000
[    1.110000] dma_buf alloc ok!
[    1.120000] hub 1-0:1.0: USB hub found
[    1.120000] hub 1-0:1.0: 1 port detected
[    1.130000] musb-hdrc musb-hdrc: USB Host mode controller at f0006000 using PIO, IRQ 26
[    1.140000] platform add gk7101 musb...
[    1.140000] mousedev: PS/2 mouse device common for all mice
[    1.150000] input: GKInput as /devices/virtual/input/input0
[    1.160000] evbug: Connected device: input0 (GKInput at gk7101/input0)
[    1.160000] Protocol NEC[0]
[    1.160000] ir request irq: 62 
[    1.160000] IR Host Controller probed!
[    1.170000] gk7101 rtc init...
[    1.170000] rtc base: 0xf2080000 
[    1.170000] os read tm: t=0 
[    1.180000] gk7101-rtc: dev (254:0)
[    1.180000] gk7101-rtc gk7101-rtc: rtc core: registered gk7101-rtc as rtc0
[    1.180000] i2c /dev entries driver
[    1.190000] gk7101_wdt: GK7101 Watchdog Timer, (c) 2014 Goke Microelectronics
[    1.200000] [gk7101_wdt_init]: init
[    1.200000] [gk7101_wdt_probe]: probe
[    1.200000] [gk7101_wdt_probe]: probe mapped wdt_base=f3006000
[    1.210000] watchdog inactive, reset disabled, irq disabled
[    1.220000] IPv4 over IPv4 tunneling driver
[    1.220000] gre: GRE over IPv4 demultiplexor driver
[    1.230000] ip_gre: GRE over IPv4 tunneling driver
[    1.240000] TCP: cubic registered
[    1.240000] Initializing XFRM netlink socket
[    1.250000] NET: Registered protocol family 10
[    1.260000] IPv6 over IPv4 tunneling driver
[    1.260000] NET: Registered protocol family 17
[    1.270000] NET: Registered protocol family 15
[    1.270000] lib80211: common routines for IEEE802.11 drivers
[    1.280000] lib80211_crypt: registered algorithm 'NULL'
[    1.280000] Registering the dns_resolver key type
[    1.280000] VFP support v0.3: implementor 41 architecture 1 part 20 variant b rev 5
[    1.290000] os read tm: t=0 
[    1.300000] gk7101-rtc gk7101-rtc: setting system clock to 1970-01-01 00:00:00 UTC (0)
[    1.310000] net eth0: ###### GKETH_start_hw
[    1.320000] net eth0: ###### GKETH_phy_start_aneg...
[    1.320000] ADDRCONF(NETDEV_UP): eth0: link is not ready
[    1.590000] usb 1-1: new high-speed USB device number 2 using musb-hdrc
[    3.350000] IP-Config: Complete:
[    3.350000]      device=eth0, addr=192.168.1.229, mask=255.255.255.0, gw=192.168.1.1
[    3.360000]      host="gk7101", domain=, nis-domain=(none)
[    3.360000]      bootserver=192.168.1.225, rootserver=192.168.1.225, rootpath=
[    3.380000] VFS: Mounted root (squashfs filesystem) readonly on device 31:3.
[    3.390000] Freeing init memory: 128K
[    8.510000] gk_vi_init
[    8.510000]  request_irq...24 ok-- video_sync
[    8.510000]  request_irq...59 ok-- video_frame_last_pixel
[    8.530000]  request_irq...61 ok-- video_frame
[    8.530000]  gk7101_is_valid_gpio_irq...
[    8.730000] crypto initialized (10:11)
Media driver version (gcc version 4.6.1 (crosstool-NG 1.18.0) (uClibc)) v1.1.2 #svn r8850 Wed Jul 6 17:44:23 CST 2016
[    8.960000] Init software HR timer for DSP communication
[   11.730000] rtusb init rt2870 --->
[   11.730000] 
[   11.730000] 
[   11.730000] === pAd = 82a82000, size = 1581168 ===
[   11.730000] 
[   11.760000] <-- RTMPAllocTxRxRingMemory, Status=0
[   11.760000] <-- RTMPAllocAdapterBlock, Status=0
[   11.780000] RTMP_COM_IoctlHandle():pAd->BulkOutEpAddr=0x8
[   11.780000] RTMP_COM_IoctlHandle():pAd->BulkOutEpAddr=0x4
[   11.790000] RTMP_COM_IoctlHandle():pAd->BulkOutEpAddr=0x5
[   11.800000] RTMP_COM_IoctlHandle():pAd->BulkOutEpAddr=0x6
[   11.810000] RTMP_COM_IoctlHandle():pAd->BulkOutEpAddr=0x7
[   11.810000] RTMP_COM_IoctlHandle():pAd->BulkOutEpAddr=0x9
[   11.820000] STA Driver version-JEDI.MP1.mt7601u.v1.5
[   11.830000] Compile time-Jul 26 2006,19:39:19
[   11.830000] ==>WaitForAsicReady MAC_CSR0=0x76010500
[   11.840000] ==>WaitForAsicReady MAC_CSR0=0x76010500
[   11.850000] NVM is EFUSE
[   11.850000] Endpoint(8) is for In-band Command
[   11.850000] Endpoint(4) is for WMM0 AC0
[   11.860000] Endpoint(5) is for WMM0 AC1
[   11.860000] Endpoint(6) is for WMM0 AC2
[   11.880000] Endpoint(7) is for WMM0 AC3
[   11.880000] Endpoint(9) is for WMM1 AC0
[   11.880000] Endpoint(84) is for Data-In
[   11.890000] Endpoint(85) is for Command Rsp
[   11.900000] 80211> RFICType = 3
[   11.900000] NumOfChan ===> 58
[   11.900000] 80211> Number of channel = 0x44
[   11.910000] 80211> Number of rate = 12
[   11.910000] 80211> CurTxPower = 0 dBm
[   11.920000] 80211> TxStream = 0
[   11.920000] crda> requlation requestion by core: 00
[   11.940000] 80211> CFG80211_Register
[   11.940000] MSC msc_proc_create: 82a82000
[   11.970000] usbcore: registered new interface driver rt2870
[   16.640000] db_max 0x2379b664, db_step 0x0
[   16.640000] sensor board reset...
[   16.970000] sensor board reset...
[   17.370000] write: addr 0x3640 val 0x3
[   20.570000] [sc1135_set_video_mode 1188] 1
[   21.020000] ================> UP : RTMP_SEM_EVENT_WAIT(STA)
[   21.020000] 1. LDO_CTR0(6c) = a6478d, PMU_OCLEVEL 6
[   21.030000] 2. LDO_CTR0(6c) = a6478d, PMU_OCLEVEL 6
[   21.040000] ==>WaitForAsicReady MAC_CSR0=0x76010500
[   21.050000] RTMP_TimerListAdd: add timer obj 82baa764!
[   21.060000] RTMP_TimerListAdd: add timer obj 82baa794!
[   21.070000] RTMP_TimerListAdd: add timer obj 82baa7c4!
[   21.070000] RTMP_TimerListAdd: add timer obj 82baa734!
[   21.080000] RTMP_TimerListAdd: add timer obj 82baa6a4!
[   21.090000] RTMP_TimerListAdd: add timer obj 82baa6d4!
[   21.100000] RTMP_TimerListAdd: add timer obj 82b3ecdc!
[   21.110000] RTMP_TimerListAdd: add timer obj 82b2b5d0!
[   21.110000] RTMP_TimerListAdd: add timer obj 82b2b604!
[   21.120000] RTMP_TimerListAdd: add timer obj 82b3ed7c!
[   21.130000] RTMP_TimerListAdd: add timer obj 82b2df80!
[   21.130000] RTMP_TimerListAdd: add timer obj 82b2d7c0!
[   21.150000] RTMP_TimerListAdd: add timer obj 82b2df4c!
[   21.150000] RTMP_TimerListAdd: add timer obj 82b2e29c!
[   21.160000] RTMP_TimerListAdd: add timer obj 82b2dfb4!
[   21.170000] RTMP_TimerListAdd: add timer obj 82b2dfe8!
[   21.170000] RTMP_TimerListAdd: add timer obj 82b2e01c!
[   21.180000] RTMP_TimerListAdd: add timer obj 82a8640c!
[   21.190000] RTMP_TimerListAdd: add timer obj 82a85c4c!
[   21.190000] RTMP_TimerListAdd: add timer obj 82a863d8!
[   21.200000] RTMP_TimerListAdd: add timer obj 82a86728!
[   21.210000] RTMP_TimerListAdd: add timer obj 82a8665c!
[   21.210000] RTMP_TimerListAdd: add timer obj 82abd684!
[   21.220000] RTMP_TimerListAdd: add timer obj 82abcec4!
[   21.230000] RTMP_TimerListAdd: add timer obj 82abd650!
[   21.230000] RTMP_TimerListAdd: add timer obj 82abd9a0!
[   21.240000] RTMP_TimerListAdd: add timer obj 82abd6b8!
[   21.250000] RTMP_TimerListAdd: add timer obj 82abd6ec!
[   21.260000] RTMP_TimerListAdd: add timer obj 82abd720!
[   21.260000] RTMP_TimerListAdd: add timer obj 82b3ec7c!
[   21.270000] RTMP_TimerListAdd: add timer obj 82b3ed4c!
[   21.280000] RTMP_TimerListAdd: add timer obj 82c01d20!
[   21.290000] RTMP_TimerListAdd: add timer obj 82c01d50!
[   21.290000] RTMP_TimerListAdd: add timer obj 82c01d80!
[   21.300000] RTMP_TimerListAdd: add timer obj 82c01db0!
[   21.310000] RTMP_TimerListAdd: add timer obj 82c01de0!
[   21.320000] RTMP_TimerListAdd: add timer obj 82c01e14!
[   21.330000] RTMP_TimerListAdd: add timer obj 82baa704!
[   21.330000] RTMP_TimerListAdd: add timer obj 82b2a5ec!
[   21.340000] RTMP_TimerListAdd: add timer obj 82b2a5bc!
[   21.350000] RTMP_TimerListAdd: add timer obj 82b2a58c!
[   21.360000] RTMP_TimerListAdd: add timer obj 82b3ecac!
[   21.370000] P2pGroupTabInit .  
[   21.370000] P2pScanChannelDefault <=== count = 3, Channels are 1, 6,11 separately   
[   21.380000] P2pCfgInit:: 
[   21.390000] ==>WaitForAsicReady MAC_CSR0=0x76010500
[   21.870000] cfg_mode=9
[   21.870000] cfg_mode=9
[   21.870000] wmode_band_equal(): Band Equal!
[   21.880000] Key1Str is Invalid key length(0) or Type(0)
[   21.890000] Key2Str is Invalid key length(0) or Type(0)
[   21.910000] Key3Str is Invalid key length(0) or Type(0)
[   21.910000] Key4Str is Invalid key length(0) or Type(0)
[   21.920000] ###### Force at HT20 (BW_20) mode !!! ########
[   21.940000] 1. Phy Mode = 14
[   21.940000] 2. Phy Mode = 14
[   21.950000] NVM is Efuse and its size =1d[1e0-1fc] 
[   21.960000] ERROR!!! MT7601 E2PROM: WRONG VERSION 0xc, should be 9
[   22.000000] 3. Phy Mode = 14
[   22.000000] AntCfgInit: primary/secondary ant 0/1
[   22.220000] ---> InitFrequencyCalibration
[   22.220000] InitFrequencyCalibrationMode:Unknow mode = 3
[   22.230000] InitFrequencyCalibration: frequency offset in the EEPROM = 125(0x7d)
[   22.240000] <--- InitFrequencyCalibration
[   22.250000] RTMPSetPhyMode: channel is out of range, use first channel=1 
[   22.270000] MCS Set = ff 00 00 00 01
[   22.290000] <==== STA : rt28xx_init, Status=0
[   22.300000] 80211> re-init bands...
[   22.330000] 80211> RFICType = 1
[   22.330000] NumOfChan ===> 14
[   22.330000] 80211> Number of channel = 0x44
[   22.360000] 80211> Number of rate = 12
[   22.360000] 80211> CurTxPower = 0 dBm
[   22.360000] 80211> TxStream = 1
[   22.390000] 0x1300 = 00064300
[   22.390000] RTMPDrvOpen(1):Check if PDMA is idle!
[   22.410000] RTMPDrvOpen(2):Check if PDMA is idle!
[   22.410000] <================ UP : RTMP_SEM_EVENT_UP(STA)
[   22.500000] net eth0: ###### GKETH_phy_stop
[   22.570000] net eth0: ###### GKETH_start_hw
[   22.570000] net eth0: ###### GKETH_phy_start_aneg...
[   22.580000] ADDRCONF(NETDEV_UP): eth0: link is not ready
[   25.570000] fps is 25, support max shutter time is 20480000 curr shutter_time 0
[   25.730000] mirror_patter 0
[   25.930000] -----------------zhangbin002-------------
[   26.130000] fps is 15, support max shutter time is 34133333 curr shutter_time 20480000
[   26.450000] win_height:0 win_width:0
[   26.450000] win_height:0 win_width:0
[   26.710000] ==>rt_ioctl_siwfreq::SIOCSIWFREQ(Channel=1)
[   26.770000] PeerBeaconAtJoinAction(): HT-CtrlChannel=1, CentralChannel=>1
[   26.790000] PeerBeaconAtJoinAction(): Set CentralChannel=1
[   27.470000] delay mod0 ret 41
[   27.470000] delay mod0 ret 45
[   27.560000] RTMP_TimerListAdd: add timer obj 82bfa518!
[   28.040000] delay mod0 ret 12
[   28.440000] delay mod0 ret 12
[   28.840000] delay mod0 ret 11
[   29.240000] delay mod0 ret 12
[   29.640000] delay mod0 ret 11
[   30.040000] delay mod0 ret 13
[   30.450000] delay mod0 ret 21
[   30.840000] delay mod0 ret 19
[   31.400000] Rcv Wcid(1) AddBAReq
[   31.420000] Start Seq = 00000000
[   31.420000] RTMP_TimerListAdd: add timer obj 82bfc528!
[   31.840000] Rcv Wcid(1) AddBAReq
[   31.860000] Start Seq = 00000000
[   31.860000] RTMP_TimerListAdd: add timer obj 82bfc57c!
[   32.570000] wlan0: no IPv6 routers present
[   33.450000] RTMP_TimerListAdd: add timer obj 82bfa558!
```

