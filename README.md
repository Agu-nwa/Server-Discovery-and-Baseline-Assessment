# Server-Discovery-and-Baseline-Assessment

## ⚙️SSH Login

### Command
```bash
chmod 400 ~/Documents/port.pem
charles@Dev ~ % ssh -i ~/Documents/port.pem ubuntu@44.205.4.102
The authenticity of host '44.205.4.102 (44.205.4.102)' can't be established.
ED25519 key fingerprint is SHA256:TMelRIwMxemVWuC3bmZYct2LIKKtQHFZTnZTx2sP4l0.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '44.205.4.102' (ED25519) to the list of known hosts.
Welcome to Ubuntu 26.04 LTS (GNU/Linux 7.0.0-1006-aws x86_64)

 * Documentation:  https://docs.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Mon Jul  6 21:44:47 UTC 2026

  System load:  0.0               Temperature:           -273.1 C
  Usage of /:   31.1% of 6.61GB   Processes:             116
  Memory usage: 27%               Users logged in:       0
  Swap usage:   0%                IPv4 address for ens5: 172.31.9.50

 * Ubuntu Pro delivers the most comprehensive open source security and
   compliance features.

   https://ubuntu.com/aws/pro

Expanded Security Maintenance for Applications is not enabled.

0 updates can be applied immediately.

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


The list of available updates is more than a week old.
To check for new updates run: sudo apt update

Last login: Mon Jul  6 14:18:30 2026 from 18.206.107.
```

## ⚙️ Check User

### Command
```bash
whoami
ubuntu
ubuntu@ip-172-31-9-50:~$
```

## ⚙️ Check Hostname

### Command
```bash
hostname
ip-172-31-9-50
ubuntu@ip-172-31-9-50:~$
```

## ⚙️ Check Linux Distribution

### Command
```bash
cat /etc/os-release
PRETTY_NAME="Ubuntu 26.04 LTS"
NAME="Ubuntu"
VERSION_ID="26.04"
VERSION="26.04 LTS (Resolute Raccoon)"
VERSION_CODENAME=resolute
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=resolute
LOGO=ubuntu-logo
ubuntu@ip-172-31-9-50:~$
```

## Check Kernel Version

### Command
```bash
uname -r
7.0.0-1006-aws
ubuntu@ip-172-31-9-50:~$
```

## Check Where you are

### Command
```bash
pwd
/home/ubuntu
ubuntu@ip-172-31-9-50:~$
```

## Inspect Root File

### Command
```bash
ls -lah /
total 68K
drwxr-xr-x  19 root root 4.0K Jul  6 13:55 .
drwxr-xr-x  19 root root 4.0K Jul  6 13:55 ..
lrwxrwxrwx   1 root root    7 Apr 20 08:46 bin -> usr/bin
drwxr-xr-x   5 root root 4.0K Jun  4 05:54 boot
drwxr-xr-x  16 root root 3.4K Jul  6 13:55 dev
drwxr-xr-x 108 root root 4.0K Jul  6 13:55 etc
drwxr-xr-x   3 root root 4.0K Jul  6 13:55 home
lrwxrwxrwx   1 root root    7 Apr 20 08:46 lib -> usr/lib
lrwxrwxrwx   1 root root    9 Apr 20 08:46 lib64 -> usr/lib64
drwx------   2 root root  16K Jun  4 05:40 lost+found
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 media
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 mnt
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 opt
dr-xr-xr-x 175 root root    0 Jul  6 13:55 proc
drwx------   4 root root 4.0K Jul  6 13:55 root
drwxr-xr-x  31 root root  940 Jul  6 14:18 run
lrwxrwxrwx   1 root root    8 Apr 20 08:46 sbin -> usr/sbin
drwxr-xr-x   6 root root 4.0K Jun  4 05:54 snap
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 srv
dr-xr-xr-x  13 root root    0 Jul  6 13:55 sys
drwxrwxrwt  12 root root  240 Jul  6 14:01 tmp
drwxr-xr-x  12 root root 4.0K Jun  4 05:29 usr
drwxr-xr-x  13 root root 4.0K Jul  6 13:55 var
ubuntu@ip-172-31-9-50:~$ ls var
ls: cannot access 'var': No such file or directory
ubuntu@ip-172-31-9-50:~$ ls ~/var
ls: cannot access '/home/ubuntu/var': No such file or directory
ubuntu@ip-172-31-9-50:~$ ls /var
backups  cache  crash  lib  local  lock  log  mail  opt  run  snap  spool  tmp
ubuntu@ip-172-31-9-50:~$
```

## ⚙️ Check Disk Space

### Command
```bash
df -h
Filesystem       Size  Used Avail Use% Mounted on
/dev/root        6.7G  2.1G  4.6G  31% /
tmpfs            455M     0  455M   0% /dev/shm
tmpfs            182M  892K  181M   1% /run
efivarfs         128K  3.1K  120K   3% /sys/firmware/efi/efivars
tmpfs            455M     0  455M   0% /tmp
none             1.0M     0  1.0M   0% /run/credentials/systemd-journald.service
none             1.0M     0  1.0M   0% /run/credentials/systemd-resolved.service
/dev/nvme0n1p13  989M   96M  827M  11% /boot
/dev/nvme0n1p15  105M  6.3M   99M   7% /boot/efi
none             1.0M     0  1.0M   0% /run/credentials/systemd-networkd.service
none             1.0M     0  1.0M   0% /run/credentials/getty@tty1.service
none             1.0M     0  1.0M   0% /run/credentials/serial-getty@ttyS0.service
tmpfs             91M  8.0K   91M   1% /run/user/1000
ubuntu@ip-172-31-9-50:~$
```

## ⚙️ Check Memory

### Command
```bash
free -h
               total        used        free      shared  buff/cache   available
Mem:           908Mi       313Mi       363Mi       2.7Mi       342Mi       595Mi
Swap:             0B          0B          0B
ubuntu@ip-172-31-9-50:~$
```

## Check Server Uptime[how long server has been running]

### Command
```bash
uptime
 14:45:49 up 50 min,  1 user,  load average: 0.00, 0.00, 0.00
ubuntu@ip-172-31-9-50:~$
```

## ⚙️ Check Architecture

### Command
```bash
uname -m
x86_64
ubuntu@ip-172-31-9-50:~$ 

```

### Check Package Manager Location

```bash
which apt
/usr/bin/apt
ubuntu@ip-172-31-9-50:~$
```

## 🧾 Server Baseline Summary

| Item | Result|
|---|---|
| Cloud Server | AWS EC2 |
| Distribution | Ubuntu 26.04 LTS|
| Kernel Version | 7.0.0-1006-aws |
| Architecture | x86_64 |
| Hostname | ip-172-31-9-50 |
| User | ubuntu |
| Public IP | 44.205.4.102 |
| Memory / Used /Available |  908Mi / 585Mi |
| Disk Space/Used/Available |  6.7G /2.1G /4.6G |
| Uptime | 50 min |
| Load Average |  0.00, 0.00, 0.00 |
| Package Manager | apt |


# File System

## ⚙️ Inspect Root Directory

### Command
```bash
ls -lah /
total 68K
drwxr-xr-x  19 root root 4.0K Jul  7 04:06 .
drwxr-xr-x  19 root root 4.0K Jul  7 04:06 ..
lrwxrwxrwx   1 root root    7 Apr 20 08:46 bin -> usr/bin
drwxr-xr-x   5 root root 4.0K Jul  7 06:50 boot
drwxr-xr-x  16 root root 3.4K Jul  7 04:06 dev
drwxr-xr-x 108 root root 4.0K Jul  7 06:51 etc
drwxr-xr-x   3 root root 4.0K Jul  6 13:55 home
lrwxrwxrwx   1 root root    7 Apr 20 08:46 lib -> usr/lib
lrwxrwxrwx   1 root root    9 Apr 20 08:46 lib64 -> usr/lib64
drwx------   2 root root  16K Jun  4 05:40 lost+found
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 media
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 mnt
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 opt
dr-xr-xr-x 175 root root    0 Jul  7 04:05 proc
drwx------   4 root root 4.0K Jul  6 13:55 root
drwxr-xr-x  33 root root 1.1K Jul  8 06:33 run
lrwxrwxrwx   1 root root    8 Apr 20 08:46 sbin -> usr/sbin
drwxr-xr-x   6 root root 4.0K Jun  4 05:54 snap
drwxr-xr-x   2 root root 4.0K Jun  4 05:29 srv
dr-xr-xr-x  13 root root    0 Jul  7 04:05 sys
drwxrwxrwt  13 root root  260 Jul  8 00:48 tmp
drwxr-xr-x  12 root root 4.0K Jun  4 05:29 usr
drwxr-xr-x  13 root root 4.0K Jul  6 13:55 var
ubuntu@ip-172-31-9-50:~$
```

## ⚙️ Check System Configuration Files

### Command
```bash
ls -lah /etc
total 940K
drwxr-xr-x 108 root root      4.0K Jul  7 06:51 .
drwxr-xr-x  19 root root      4.0K Jul  7 04:06 ..
-rw-------   1 root root         0 Jun  4 05:29 .pwd.lock
-rw-r--r--   1 root root       862 Jun  4 05:29 .resolv.conf.systemd-resolved.bak
-rw-r--r--   1 root root       255 Jun  4 05:29 .updated
drwxr-xr-x   5 root root      4.0K Jun  4 05:39 ModemManager
drwxr-xr-x   2 root root      4.0K Jun  4 05:40 PackageKit
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 X11
drwxr-xr-x   4 root root      4.0K Jun  4 05:54 acpi
-rw-r--r--   1 root root      4.0K Nov  4  2025 adduser.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:42 alternatives
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 apparmor
drwxr-xr-x   9 root root      4.0K Jun  4 05:39 apparmor.d
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 apport
drwxr-xr-x   8 root root      4.0K Jun  4 05:56 apt
-rw-r--r--   1 root root      2.5K Feb 13 12:16 bash.bashrc
-rw-r--r--   1 root root        45 Sep 28  2025 bash_completion
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 bash_completion.d
-rw-r--r--   1 root root       367 Mar 10 15:03 bindresvport.blacklist
drwxr-xr-x   2 root root      4.0K Apr 15 18:32 binfmt.d
drwxr-xr-x   3 root root      4.0K Jun  4 05:29 ca-certificates
-rw-r--r--   1 root root      6.2K Jul  7 06:51 ca-certificates.conf
-rw-r--r--   1 root root      6.1K Jun  4 05:29 ca-certificates.conf.dpkg-old
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 chrony
drwxr-xr-x   5 root root      4.0K Jun  4 05:40 cloud
drwxr-xr-x   2 root root      4.0K Jun  4 05:40 console-setup
drwx------   2 root root      4.0K Apr 15 18:32 credstore
drwx------   2 root root      4.0K Apr 15 18:32 credstore.encrypted
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 cron.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 cron.daily
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 cron.hourly
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 cron.monthly
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 cron.weekly
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 cron.yearly
-rw-r--r--   1 root root      1.2K Nov  5  2025 crontab
-rw-r--r--   1 root root        54 Jun  4 05:39 crypttab
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 dbus-1
-rw-r--r--   1 root root      2.9K Feb 16 17:48 debconf.conf
-rw-r--r--   1 root root        10 Apr 20 08:46 debian_version
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 debuginfod
drwxr-xr-x   3 root root      4.0K Jul  7 06:51 default
-rw-r--r--   1 root root      1.7K Nov  4  2025 deluser.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 depmod.d
drwxr-xr-x   3 root root      4.0K Jun  4 05:29 dhcp
-rw-r--r--   1 root root      1.3K Jan  6 21:34 dhcpcd.conf
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 dpkg
-rw-r--r--   1 root root       117 Apr 13 13:34 dracut.conf
drwxr-xr-x   2 root root      4.0K Apr 13 13:34 dracut.conf.d
-rw-r--r--   1 root root       685 Feb 13 12:17 e2scrub.conf
-rw-r--r--   1 root root        36 Jun  4 05:54 ec2_version
-rw-r--r--   1 root root       106 Jun  4 05:29 environment
-rw-r--r--   1 root root      1.9K Mar 15  2025 ethertypes
-rw-r--r--   1 root root       146 Jun  4 05:46 fstab
-rw-r--r--   1 root root       725 Mar 21 07:16 fuse.conf
drwxr-xr-x   4 root root      4.0K Jun  4 05:39 fwupd
-rw-r--r--   1 root root      2.6K Jan 23 20:54 gai.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:30 gnutls
-rw-r--r--   1 root root      3.9K Mar 15 01:33 gprofng.rc
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 groff
-rw-r--r--   1 root root       847 Jul  6 13:55 group
-rw-r--r--   1 root root       801 Jun  4 05:40 group-
drwxr-xr-x   2 root root      4.0K Jun  4 05:54 grub.d
-rw-r-----   1 root shadow     717 Jul  6 13:55 gshadow
-rw-r-----   1 root shadow     675 Jun  4 05:40 gshadow-
drwxr-xr-x   3 root root      4.0K Jun  4 05:29 gss
-rw-r--r--   1 root root      4.4K Apr 16  2024 hdparm.conf
-rw-r--r--   1 root root      1.1K May 30  2024 hibinit-config.cfg
-rw-r--r--   1 root root        92 Apr 20 08:46 host.conf
-rw-r--r--   1 root root        15 Jul  6 13:55 hostname
-rw-r--r--   1 root root       221 Jun  3 23:21 hosts
-rw-r--r--   1 root root       411 Jun  4 05:39 hosts.allow
-rw-r--r--   1 root root       711 Jun  4 05:39 hosts.deny
drwxr-xr-x   2 root root      4.0K Jul  7 06:51 init.d
drwxr-xr-x   5 root root      4.0K Jun  4 05:39 initramfs-tools
-rw-r--r--   1 root root      1.9K Feb 13 10:25 inputrc
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 iscsi
-rw-r--r--   1 root root        24 Apr 20 08:46 issue
-rw-r--r--   1 root root        17 Apr 20 08:46 issue.net
drwxr-xr-x   6 root root      4.0K Jun  4 05:53 kernel
drwxrwxr-x   2 root landscape 4.0K Mar 20 18:10 landscape
-rw-r--r--   1 root root       22K Jul  7 06:51 ld.so.cache
-rw-r--r--   1 root root        34 Mar 10 15:03 ld.so.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 ld.so.conf.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 ldap
-rw-r--r--   1 root root       267 Apr 20 08:46 legal
-rw-r--r--   1 root root       191 Mar 20 11:17 libaudit.conf
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 libblockdev
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 libibverbs.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 libnl-3
-rw-r--r--   1 root root        13 Jun  4 05:40 locale.conf
-rw-r--r--   1 root root      9.5K Jun  4 05:40 locale.gen
lrwxrwxrwx   1 root root        27 Jun  4 05:29 localtime -> /usr/share/zoneinfo/Etc/UTC
drwxr-xr-x   4 root root      4.0K Jun  4 05:39 logcheck
-rw-r--r--   1 root root      5.8K Feb  2 20:45 login.defs
-rw-r--r--   1 root root       586 Dec  6  2025 logrotate.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 logrotate.d
-rw-r--r--   1 root root       105 Apr 20 08:46 lsb-release
drwxr-xr-x   3 root root      4.0K Jun  4 05:40 lvm
-r--r--r--   1 root root        33 Jul  6 13:55 machine-id
-rw-r--r--   1 root root       111 Feb  2 20:37 magic
-rw-r--r--   1 root root       111 Feb  2 20:37 magic.mime
-rw-r--r--   1 root root      5.2K Feb  2 20:49 manpath.config
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 mdadm
-rw-r--r--   1 root root       77K Oct 14  2025 mime.types
-rw-r--r--   1 root root       775 Feb 13 12:17 mke2fs.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:53 modprobe.d
-rw-r--r--   1 root root       212 Jun  4 05:29 modules
drwxr-xr-x   2 root root      4.0K Jun  4 05:46 modules-load.d
lrwxrwxrwx   1 root root        19 Jun  4 05:29 mtab -> ../proc/self/mounts
drwx------   2 root root      4.0K Jul  6 13:55 multipath
-rw-r--r--   1 root root        41 Mar 16 17:17 multipath.conf
-rw-r--r--   1 root root       12K Nov 20  2025 nanorc
drwxr-xr-x   6 root root      4.0K Jun  4 05:39 needrestart
-rw-r--r--   1 root root       767 Mar 28 11:23 netconfig
drwxr-xr-x   2 root root      4.0K Jul  6 13:55 netplan
drwxr-xr-x   5 root root      4.0K Jun  4 05:29 network
drwxr-xr-x   8 root root      4.0K Jun  4 05:29 networkd-dispatcher
-rw-r--r--   1 root root        91 Apr 20 08:46 networks
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 newt
-rwxr-xr-x   1 root root       243 Jun 10  2025 nftables.conf
-rw-r--r--   1 root root       526 Jun  4 05:29 nsswitch.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 opt
lrwxrwxrwx   1 root root        21 Apr 24 10:24 os-release -> ../usr/lib/os-release
-rw-r--r--   1 root root      7.0K Apr 16 14:00 overlayroot.conf
-rw-r--r--   1 root root       112 Jun  4 05:40 overlayroot.local.conf
-rw-r--r--   1 root root       552 Jul  3  2025 pam.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 pam.d
-rw-r--r--   1 root root      1.8K Jul  6 13:55 passwd
-rw-r--r--   1 root root      1.8K Jun  4 05:54 passwd-
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 perl
drwxr-xr-x   4 root root      4.0K Jun  4 05:39 pki
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 plymouth
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 pm
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 polkit-1
drwxr-xr-x   2 root root      4.0K Mar 31 12:31 pollinate
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 ppp
-rw-r--r--   1 root root       641 Apr 20 08:46 profile
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 profile.d
-rw-r--r--   1 root root      3.1K Oct 17  2022 protocols
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 python3
drwxr-xr-x   2 root root      4.0K Jul  7 06:49 python3.14
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc0.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc1.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc2.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc3.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc4.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc5.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:56 rc6.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 rcS.d
lrwxrwxrwx   1 root root        39 Jun  4 05:29 resolv.conf -> ../run/systemd/resolve/stub-resolv.conf
lrwxrwxrwx   1 root root        13 Jun 27 23:09 rmt -> /usr/sbin/rmt
-rw-r--r--   1 root root       911 Oct 17  2022 rpc
-rw-r--r--   1 root root      1.2K Aug 21  2025 rsyslog.conf
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 rsyslog.d
-rw-r--r--   1 root root      3.6K Sep 19  2025 screenrc
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 security
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 selinux
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 sensors.d
-rw-r--r--   1 root root       11K Feb  2 20:46 sensors3.conf
-rw-r--r--   1 root root       13K Mar 15  2025 services
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 sgml
-rw-r-----   1 root shadow     877 Jul  6 13:55 shadow
-rw-r-----   1 root shadow     877 Jul  6 13:55 shadow-
-rw-r--r--   1 root root       148 Jul  7 06:51 shells
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 skel
drwxr-xr-x   6 root root      4.0K Jun  4 05:39 sos
drwxr-xr-x   4 root root      4.0K Jul  6 13:55 ssh
drwxr-xr-x   4 root root      4.0K Jul  7 06:49 ssl
-rw-r--r--   1 root root        20 Jul  6 13:55 subgid
-rw-r--r--   1 root root         0 Jun  4 05:29 subgid-
-rw-r--r--   1 root root        20 Jul  6 13:55 subuid
-rw-r--r--   1 root root         0 Jun  4 05:29 subuid-
-rw-r--r--   1 root root      4.3K Mar 13 11:02 sudo.conf
-rw-r--r--   1 root root      9.6K Mar 13 11:02 sudo_logsrvd.conf
-r--r-----   1 root root      1.8K Jan 21 15:09 sudoers
drwxr-x---   2 root root      4.0K Jul  6 13:55 sudoers.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 supercat
drwxr-xr-x   2 root root      4.0K Jun  4 05:46 sysctl.d
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 sysstat
drwxr-xr-x   7 root root      4.0K Jun  4 05:40 systemd
drwxr-xr-x   2 root root      4.0K Jun  4 05:29 terminfo
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 tmpfiles.d
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 tpm2-tss
drwxr-xr-x   2 root root      4.0K Jun  4 05:30 ubuntu-advantage
-rw-r--r--   1 root root      1.3K Feb 26 13:38 ucf.conf
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 udev
drwxr-xr-x   2 root root      4.0K Jun  4 05:39 udisks2
drwxr-xr-x   3 root root      4.0K Jun  4 05:39 ufw
drwxr-xr-x   3 root root      4.0K Jun  4 05:40 update-manager
drwxr-xr-x   2 root root      4.0K Jun  4 05:40 update-motd.d
drwxr-xr-x   2 root root      4.0K Apr 16 19:14 update-notifier
-rw-r--r--   1 root root      1.5K Dec  1  2025 usb_modeswitch.conf
drwxr-xr-x   2 root root      4.0K Dec  6  2025 usb_modeswitch.d
lrwxrwxrwx   1 root root        16 Jun  4 05:29 vconsole.conf -> default/keyboard
drwxr-xr-x   2 root root      4.0K Jul  7 06:51 vim
drwxr-xr-x   4 root root      4.0K Jun  4 05:39 vmware-tools
lrwxrwxrwx   1 root root        23 Mar  2 14:21 vtrgb -> /etc/alternatives/vtrgb
-rw-r--r--   1 root root      4.9K Feb  2 20:52 wgetrc
-rw-r--r--   1 root root       681 Feb 15 13:26 xattr.conf
drwxr-xr-x   4 root root      4.0K Jun  4 05:29 xdg
drwxr-xr-x   2 root root      4.0K Jun  4 05:40 xml
-rw-r--r--   1 root root       460 Jan 20  2023 zsh_command_not_found
ubuntu@ip-172-31-9-50:~$ 
```

## ⚙️ Check Changing System Data

### Command
```bash
ls -lah /var
total 56K
drwxr-xr-x 13 root root   4.0K Jul  6 13:55 .
drwxr-xr-x 19 root root   4.0K Jul  7 04:06 ..
-rw-r--r--  1 root root    255 Jun  4 05:29 .updated
drwxr-xr-x  2 root root   4.0K Jul  8 00:00 backups
drwxr-xr-x 16 root root   4.0K Jul  6 14:50 cache
drwxrwxrwt  2 root root   4.0K Jun  4 05:39 crash
drwxr-xr-x 48 root root   4.0K Jul  7 06:51 lib
drwxr-xr-x  2 root root   4.0K Apr 20 08:46 local
lrwxrwxrwx  1 root root      9 Jun  4 05:29 lock -> /run/lock
drwxrwxr-x 11 root syslog 4.0K Jul  7 04:06 log
drwxrwsr-x  2 root mail   4.0K Jun  4 05:29 mail
drwxr-xr-x  2 root root   4.0K Jun  4 05:29 opt
lrwxrwxrwx  1 root root      4 Jun  4 05:29 run -> /run
drwxr-xr-x  5 root root   4.0K Jun  4 05:54 snap
drwxr-xr-x  4 root root   4.0K Jun  4 05:29 spool
drwxrwxrwt  9 root root   4.0K Jul  8 00:48 tmp
ubuntu@ip-172-31-9-50:~$ 
```
## ⚙️ Check Log Files

### Command
```bash
ls -lah /var/log
total 1.5M
drwxrwxr-x 11 root      syslog          4.0K Jul  7 04:06 .
drwxr-xr-x 13 root      root            4.0K Jul  6 13:55 ..
lrwxrwxrwx  1 root      root              39 Jun  4 05:29 README -> ../../usr/share/doc/systemd/README.logs
-rw-r--r--  1 root      root            8.8K Jul  7 06:51 alternatives.log
drwx------  3 root      root            4.0K Jul  6 13:55 amazon
-rw-r-----  1 root      adm                0 Jul  6 13:55 apport.log
drwxr-xr-x  2 root      root            4.0K Jul  7 06:51 apt
-rw-r-----  1 syslog    adm             115K Jul  8 06:51 auth.log
-rw-rw----  1 root      utmp               0 Jun  4 05:40 btmp
drwxr-x---  2 _chrony   _chrony         4.0K Jul  6 13:55 chrony
-rw-r-----  1 root      adm             4.5K Jul  7 04:06 cloud-init-output.log
-rw-r-----  1 syslog    adm             282K Jul  7 04:06 cloud-init.log
drwxr-xr-x  2 root      root            4.0K Apr 22 17:29 dist-upgrade
-rw-r-----  1 root      adm              49K Jul  7 04:06 dmesg
-rw-r-----  1 root      adm              51K Jul  6 13:55 dmesg.0
-rw-r--r--  1 root      root             67K Jul  7 06:51 dpkg.log
drwxr-sr-x+ 3 root      systemd-journal 4.0K Jul  6 13:55 journal
-rw-r-----  1 syslog    adm             137K Jul  8 06:33 kern.log
drwxr-xr-x  2 landscape landscape       4.0K Jul  6 13:56 landscape
-rw-rw-r--  1 root      utmp            286K Jul  8 06:33 lastlog
drwx------  2 root      root            4.0K Jul  6 13:55 private
-rw-r-----  1 syslog    adm             698K Jul  8 07:00 syslog
drwxr-xr-x  2 root      root            4.0K Jul  8 00:07 sysstat
drwxr-x---  2 root      adm             4.0K Jul  6 23:11 unattended-upgrades
-rw-rw-r--  1 root      utmp            6.8K Jul  8 06:33 wtmp
```
