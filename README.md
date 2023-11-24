# Orange Pi 5+ (RK3588) experiments
I got a new Orange Pi 5+, and I'm having fun from playing with it.

This is the repo for record something to not forget when I finished everything.

## neofetch
```
            .-/+oossssoo+/-.               orangepi@orangepi5plus
        `:+ssssssssssssssssss+:`           ----------------------
      -+ssssssssssssssssssyyssss+-         OS: Ubuntu 22.04.3 LTS aarch64
    .ossssssssssssssssssdMMMNysssso.       Host: RK3588 OPi 5 Plus
   /ssssssssssshdmmNNmmyNMMMMhssssss/      Kernel: 5.10.110+
  +ssssssssshmydMMMMMMMNddddyssssssss+     Uptime: 10 mins
 /sssssssshNMMMyhhyyyyhmNMMMNhssssssss/    Packages: 1881 (dpkg)
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Shell: bash 5.1.16
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   Resolution: 3840x2160
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   Terminal: /dev/pts/0
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   CPU: (8) @ 1.800GHz
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   GPU: AMD ATI Radeon 540/540X/550/550X / RX 540X/550/550X 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Memory: 362MiB / 15719MiB
 /sssssssshNMMMyhhyyyyhdNMMMNhssssssss/
  +sssssssssdmydMMMMMMMMddddyssssssss+
   /ssssssssssshdmNNNNmyNMMMMhssssss/
    .ossssssssssssssssssdMMMNysssso.
      -+sssssssssssssssssyyyssss+-
        `:+ssssssssssssssssss+:`
            .-/+oossssoo+/-.
```
Ignore GPU section lol

## eMMC
```
/dev/mmcblk0:
 Timing O_DIRECT disk reads: 688 MB in  3.01 seconds = 228.92 MB/sec
andrew@andrew-desktop:~$ sudo hdparm -t --direct /dev/mmcblk0

/dev/mmcblk0:
 Timing O_DIRECT disk reads: 716 MB in  3.00 seconds = 238.35 MB/sec
andrew@andrew-desktop:~$
```

## NVMe Disk
```
andrew@andrew-desktop:~$ sudo hdparm -t --direct /dev/nvme0n1

/dev/nvme0n1:
 Timing O_DIRECT disk reads: 5348 MB in  3.00 seconds = 1782.51 MB/sec
andrew@andrew-desktop:~$ sudo hdparm -t --direct /dev/nvme0n1

/dev/nvme0n1:
 Timing O_DIRECT disk reads: 5538 MB in  3.00 seconds = 1845.76 MB/sec
andrew@andrew-desktop:~$ sudo hdparm -t --direct /dev/nvme0n1

/dev/nvme0n1:
 Timing O_DIRECT disk reads: 5512 MB in  3.00 seconds = 1836.86 MB/sec
```
