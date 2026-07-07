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
