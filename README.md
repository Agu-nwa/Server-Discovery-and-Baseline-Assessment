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

## ⚙️ Check Linux Disto

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

## ⚙️ List Everything under Root

### Command
```bash
ls /*
/bin:
 3cpio                                glib-compile-schemas   ldattach                           py3versions            strip
 VGAuthService                        'gnu['                 ldd                                pybabel                stty
 '['                                  gnuarch                less                               pybabel-python3        su
 aa-enabled                           gnub2sum               lessecho                           pydoc3                 su-rs
 aa-exec                              gnubase32              lessfile                           pydoc3.14              sudo
 aa-features-abi                      gnubase64              lesskey                            pygettext3             sudo-rs
 acpi_listen                          gnubasename            lesspipe                           pygettext3.14          sudo.ws
 acpidbg                              gnubasenc              lexgrog                            pygmentize             sudoedit
 add-apt-repository                   gnucat                 libnetcfg                          pyhtmlizer3            sudoedit-rs
 addpart                              gnuchcon               link                               pyserial-miniterm      sudoreplay.ws
 addr2line                            gnuchgrp               linux-boot-prober                  pyserial-ports         sum
 apport-bug                           gnuchmod               linux-check-removal                python3                switch_root
 apport-cli                           gnuchown               linux-run-hooks                    python3.14             sync
 apport-collect                       gnucksum               linux-update-symlinks              pzstd                  systemctl
 apport-unpack                        gnucomm                linux-version                      qmi-firmware-update    systemd-ac-power
 appstreamcli                         gnucp                  linux32                            qmi-network            systemd-analyze
 apropos                              gnucsplit              linux64                            qmicli                 systemd-ask-password
 apt                                  gnucut                 ln                                 ranlib                 systemd-cat
 apt-add-repository                   gnudate                lnstat                             rbash                  systemd-cgls
 apt-cache                            gnudd                  loadkeys                           rdma                   systemd-cgtop
 apt-cdrom                            gnudf                  loadunimap                         readelf                systemd-confext
 apt-config                           gnudir                 locale                             readlink               systemd-creds
 apt-get                              gnudircolors           locale-check                       realpath               systemd-cryptenroll
 apt-mark                             gnudirname             localectl                          red                    systemd-cryptsetup
 ar                                   gnudu                  localedef                          rename.ul              systemd-delta
 arch                                 gnuecho                logger                             renice                 systemd-detect-virt
 as                                   gnuenv                 login                              rescan-scsi-bus.sh     systemd-escape
 automat-visualize3                   gnuexpand              loginctl                           reset                  systemd-firstboot
 awk                                  gnuexpr                logname                            resizecons             systemd-hwdb
 b2sum                                gnufactor              look                               resizepart             systemd-id128
 base32                               gnufalse               lowntfs-3g                         resolvectl             systemd-inhibit
 base64                               gnufmt                 ls                                 rev                    systemd-machine-id-setup
 basename                             gnufold                lsattr                             rgrep                  systemd-mount
 basenc                               gnugroups              lsb_release                        rm                     systemd-mute-console
 bash                                 gnuhead                lsblk                              rmdir                  systemd-notify
 bashbug                              gnuhostid              lsclocks                           rnano                  systemd-path
 bc                                   gnuid                  lscpu                              routel                 systemd-pty-forward
 bits                                 gnuinstall             lsfd                               rrsync                 systemd-run
 blkzone                              gnujoin                lshw                               rsync                  systemd-socket-activate
 boltctl                              gnulink                lsinitramfs                        rsync-ssl              systemd-stdio-bridge
 bpftrace                             gnuln                  lsinitrd                           rtla                   systemd-sysext
 bpftrace-aotrt                       gnulogname             lsipc                              rtstat                 systemd-sysusers
 btrfs                                gnuls                  lsirq                              run-parts              systemd-tmpfiles
 btrfs-convert                        gnumd5sum              lslocks                            run0                   systemd-tty-ask-password-agent
 btrfs-find-root                      gnumkdir               lslogins                           runcon                 systemd-umount
 btrfs-image                          gnumkfifo              lsmem                              rview                  systemd-vpick
 btrfs-map-logical                    gnumknod               lsmod                              rvim                   tabs
 btrfs-select-super                   gnumktemp              lsns                               sadf                   tac
 btrfsck                              gnumv                  lsof                               sar                    tail
 btrfstune                            gnunice                lspci                              sar.sysstat            tapestat
 busctl                               gnunl                  lspgpot                            savelog                tar
 busybox                              gnunohup               lspower                            sbattach               taskset
 c++filt                              gnunproc               lsusb                              sbkeysync              tbl
 c_rehash                             gnunumfmt              lzcat                              sbsiglist              tclsh
 captoinfo                            gnuod                  lzcmp                              sbsign                 tclsh8.6
 cat                                  gnupaste               lzdiff                             sbvarsign              tcpdump
 catman                               gnupathchk             lzegrep                            sbverify               tee
 cftp3                                gnupinky               lzfgrep                            scalar                 telnet
 chage                                gnupr                  lzgrep                             scp                    tempfile
 chardet                              gnuprintenv            lzless                             screen                 test
 chardetect                           gnuprintf              lzma                               screendump             tic
 chattr                               gnuptx                 lzmainfo                           script                 time
 chcon                                gnupwd                 lzmore                             scriptlive             timedatectl
 chcpu                                gnureadlink            mailmail3                          scriptreplay           timeout
 chfn                                 gnurealpath            man                                scsi_logging_level     tkconch3
 chgrp                                gnurm                  man-recode                         scsi_mandat            tload
 chmem                                gnurmdir               mandb                              scsi_readcap           tmux
 chmod                                gnuruncon              manpath                            scsi_ready             tnftp
 choom                                gnuseq                 mapscrn                            scsi_satl              toe
 chown                                gnusha1sum             markdown-it                        scsi_start             top
 chronyc                              gnusha224sum           mawk                               scsi_stop              touch
 chroot                               gnusha256sum           mbim-network                       scsi_temperature       tput
 chrt                                 gnusha384sum           mbimcli                            sdiff                  tr
 chsh                                 gnusha512sum           mcookie                            sed                    trace-cmd
 chvt                                 gnushred               md5sum                             select-editor          tracepath
 cifsiostat                           gnushuf                mdig                               sensible-browser       trial3
 ckbcomp                              gnusleep               memhog                             sensible-editor        troff
 ckeygen3                             gnusort                migrate-pubring-from-classic-gpg   sensible-pager         true
 cksum                                gnusplit               migratepages                       sensible-terminal      truncate
 clear                                gnustat                migspeed                           seq                    tset
 clear_console                        gnustdbuf              mk_modmap                          setarch                tsort
 cloud-id                             gnustty                mkdir                              setfont                tty
 cloud-init                           gnusum                 mkfifo                             setkeycodes            turbostat
 cloud-init-per                       gnusync                mknod                              setleds                twist3
 cmp                                  gnutac                 mksquashfs                         setlogcons             twistd3
 codepage                             gnutail                mktemp                             setmetamode            tzselect
 col                                  gnutee                 mmcli                              setpci                 ua
 colcrt                               gnutest                mokutil                            setpriv                ubuntu-advantage
 colrm                                gnutimeout             more                               setsid                 ubuntu-bug
 column                               gnutouch               mount                              setterm                ubuntu-distro-info
 comm                                 gnutr                  mountpoint                         setupcon               ubuntu-security-status
 conch3                               gnutrue                mpstat                             sftp                   ucf
 corelist                             gnutruncate            mt                                 sg                     ucfq
 coresched                            gnutsort               mt-gnu                             sg_bg_ctl              ucfr
 coreutils                            gnutty                 mtr                                sg_compare_and_write   uclampset
 cp                                   gnuuname               mtr-packet                         sg_copy_results        udevadm
 cpan                                 gnuunexpand            mv                                 sg_dd                  udisksctl
 cpan5.40-x86_64-linux-gnu            gnuuniq                namei                              sg_decode_sense        ul
 cpio                                 gnuunlink              nano                               sg_emc_trespass        umount
 cpupower                             gnuusers               nawk                               sg_format              uname
 crontab                              gnuvdir                nc                                 sg_get_config          unattended-upgrade
 csplit                               gnuwc                  nc.openbsd                         sg_get_elem_status     unattended-upgrades
 ctstat                               gnuwho                 neqn                               sg_get_lba_status      uncompress
 curl                                 gnuwhoami              netaddr                            sg_ident               unexpand
 cut                                  gnuyes                 netcat                             sg_inq                 unicode_start
 cvtsudoers.ws                        gp-archive             netshaper                          sg_logs                unicode_stop
 dash                                 gp-collect-app         networkctl                         sg_luns                uniq
 date                                 gp-display-html        networkd-dispatcher                sg_map                 unlink
 dbus-cleanup-sockets                 gp-display-src         newgrp                             sg_map26               unlzma
 dbus-daemon                          gp-display-text        ngettext                           sg_modes               unmkinitramfs
 dbus-monitor                         gpasswd                nice                               sg_opcodes             unshare
 dbus-run-session                     gpg                    nisdomainname                      sg_persist             unsquashfs
 dbus-send                            gpg-agent              nl                                 sg_prevent             unxz
 dbus-update-activation-environment   gpg-connect-agent      nm                                 sg_raw                 unzstd
 dbus-uuidgen                         gpg-mail-tube          nohup                              sg_rbuf                update-alternatives
 dbxtool                              gpg-wks-client         nproc                              sg_rdac                update-microcode-initrd
 dd                                   gpgconf                nroff                              sg_read                update-mime-database
 deallocvt                            gpgparsemail           nsenter                            sg_read_attr           uptime
 deb-systemd-helper                   gpgsm                  nslookup                           sg_read_block_limits   usb-devices
 deb-systemd-invoke                   gpgsplit               nstat                              sg_read_buffer         usbhid-dump
 debconf                              gpgtar                 nsupdate                           sg_read_long           usbip
 debconf-apt-progress                 gpgv                   ntfs-3g                            sg_readcap             usbipd
 debconf-communicate                  gpic                   ntfs-3g.probe                      sg_reassign            usbreset
 debconf-copydb                       gprof                  ntfscat                            sg_referrals           users
 debconf-escape                       gprofng                ntfscluster                        sg_rem_rest_elem       uuidgen
 debconf-set-selections               gprofng-archive        ntfscmp                            sg_rep_density         uuidparse
 debconf-show                         gprofng-collect-app    ntfsdecrypt                        sg_rep_pip             varlinkctl
 debian-distro-info                   gprofng-display-html   ntfsfallocate                      sg_rep_zones           vcs-run
 delpart                              gprofng-display-src    ntfsfix                            sg_requests            vdir
 delv                                 gprofng-display-text   ntfsinfo                           sg_reset               vi
 df                                   gprofng-gmon           ntfsls                             sg_reset_wp            view
 dh_bash-completion                   grep                   ntfsmove                           sg_rmsn                vim
 dh_installxmlcatalogs                gresource              ntfsrecover                        sg_rtpg                vim.basic
 diff                                 groff                  ntfssecaudit                       sg_safte               vim.tiny
 diff3                                grog                   ntfstruncate                       sg_sanitize            vimdiff
 dig                                  grops                  ntfsusermap                        sg_sat_datetime        vimtutor
 dir                                  grotty                 ntfswipe                           sg_sat_identify        visudo-rs
 dircolors                            groups                 numactl                            sg_sat_phy_event       vm-support
 dirmngr                              growpart               numastat                           sg_sat_read_gplog      vmhgfs-fuse
 dirmngr-client                       grub-editenv           numfmt                             sg_sat_set_features    vmstat
 dirname                              grub-file              objcopy                            sg_scan                vmtoolsd
 distro-info                          grub-fstest            objdump                            sg_seek                vmware-alias-import
 dmesg                                grub-glue-efi          od                                 sg_senddiag            vmware-checkvm
 dnsdomainname                        grub-kbdcomp           oem-getlogs                        sg_ses                 vmware-hgfsclient
 do-release-upgrade                   grub-menulst2cfg       on_ac_power                        sg_ses_microcode       vmware-namespace-cmd
 domainname                           grub-mkfont            openssl                            sg_start               vmware-rpctool
 dpkg                                 grub-mkimage           openvt                             sg_stpg                vmware-toolbox-cmd
 dpkg-deb                             grub-mklayout          os-prober                          sg_stream_ctl          vmware-vgauth-cmd
 dpkg-divert                          grub-mknetdir          pager                              sg_sync                vmware-vmblock-fuse
 dpkg-maintscript-helper              grub-mkpasswd-pbkdf2   partx                              sg_test_rwbuf          vmware-xferlogs
 dpkg-query                           grub-mkrelpath         passwd                             sg_timestamp           w
 dpkg-realpath                        grub-mkrescue          paste                              sg_turs                waitpid
 dpkg-split                           grub-mkstandalone      patch                              sg_unmap               wall
 dpkg-statoverride                    grub-mount             pathchk                            sg_verify              watch
 dpkg-trigger                         grub-ntldr-img         pcilmr                             sg_vpd                 watchgnupg
 dracut                               grub-render-label      pdb3                               sg_wr_mode             wc
 dracut-catimages                     grub-script-check      pdb3.14                            sg_write_attr          wcurl
 du                                   grub-syslinux2cfg      peekfd                             sg_write_buffer        wdctl
 dumpkeys                             gsettings              perf                               sg_write_long          wget
 eatmydata                            gtbl                   perl                               sg_write_same          whatis
 ec2metadata                          gunzip                 perl5.40-x86_64-linux-gnu          sg_write_verify        whereis
 echo                                 gzexe                  perl5.40.1                         sg_write_x             which
 ed                                   gzip                   perlbug                            sg_xcopy               which.debianutils
 editor                               h2ph                   perldoc                            sg_z_act_query         whiptail
 efibootdump                          h2xs                   perlivp                            sg_zone                who
 efibootmgr                           hardlink               perlthanks                         sginfo                 whoami
 egrep                                hashsum                pgrep                              sgm_dd                 x86_64
 eject                                hd                     pic                                sgp_dd                 x86_64-linux-gnu-addr2line
 elfedit                              head                   pico                               sh                     x86_64-linux-gnu-ar
 enc2xs                               helpztags              piconv                             sha1sum                x86_64-linux-gnu-as
 encguess                             hexdump                pidof                              sha224sum              x86_64-linux-gnu-c++filt
 enosys                               hibinit-agent          pidstat                            sha256sum              x86_64-linux-gnu-elfedit
 env                                  host                   pidwait                            sha3-224sum            x86_64-linux-gnu-gprof
 envsubst                             hostid                 pinentry                           sha3-256sum            x86_64-linux-gnu-ld
 eqn                                  hostname               pinentry-curses                    sha3-384sum            x86_64-linux-gnu-ld.bfd
 ex                                   hostnamectl            ping                               sha3-512sum            x86_64-linux-gnu-nm
 exch                                 htop                   ping4                              sha384sum              x86_64-linux-gnu-objcopy
 expand                               hwe-support-status     ping6                              sha3sum                x86_64-linux-gnu-objdump
 expiry                               i386                   pinky                              sha512sum              x86_64-linux-gnu-ranlib
 expr                                 iconv                  pipesz                             shake128sum            x86_64-linux-gnu-readelf
 factor                               id                     pivot_root                         shake256sum            x86_64-linux-gnu-size
 fadvise                              inetutils-telnet       pkaction                           shasum                 x86_64-linux-gnu-strings
 fallocate                            info                   pkcheck                            showconsolefont        x86_64-linux-gnu-strip
 false                                infobrowser            pkgcli                             showkey                x86_energy_perf_policy
 fgconsole                            infocmp                pkill                              shred                  xargs
 fgrep                                infotocap              pkttyagent                         shuf                   xauth
 file                                 install                pl2pm                              size                   xdg-user-dir
 finalrd                              install-info           pldd                               skill                  xdg-user-dirs-update
 fincore                              instmodsh              plymouth                           slabtop                xsubpp
 find                                 ionice                 pmap                               sleep                  xxd
 findmnt                              iostat                 pod2html                           snap                   xz
 flock                                ip                     pod2man                            snapctl                xzcat
 fmt                                  ipcmk                  pod2text                           snapfuse               xzcmp
 fold                                 ipcrm                  pod2usage                          snice                  xzdiff
 free                                 ipcs                   podchecker                         soelim                 xzegrep
 ftp                                  iptables-xml           pollinate                          sort                   xzfgrep
 fuser                                ischroot               pr                                 sos                    xzgrep
 fusermount                           iscsiadm               preconv                            splain                 xzless
 fusermount3                          isosize                printenv                           split                  xzmore
 fwupdmgr                             join                   printf                             splitfont              yes
 fwupdtool                            journalctl             prlimit                            sqfscat                ypdomainname
 gapplication                         jq                     pro                                sqfstar                zcat
 gawk                                 json-patch-jsondiff    prove                              ss                     zcmp
 gawkbug                              json_pp                prtstat                            ssh                    zdiff
 gdbus                                jsondiff               ps                                 ssh-add                zdump
 geqn                                 jsonpatch              psfaddtable                        ssh-agent              zegrep
 getconf                              jsonpointer            psfgettable                        ssh-argv0              zfgrep
 getent                               jsonschema             psfstriptable                      ssh-copy-id            zforce
 getkeycodes                          kbd_mode               psfxtable                          ssh-import-id          zgrep
 getopt                               kbdinfo                pslog                              ssh-import-id-gh       zipdetails
 gettext                              kbxutil                pstree                             ssh-import-id-lp       zless
 gettext.sh                           kernel-install         pstree.x11                         ssh-keygen             zmore
 ginstall-info                        kill                   ptar                               ssh-keyscan            znew
 gio                                  killall                ptardiff                           stat                   zstd
 gio-querymodules                     kmod                   ptargrep                           static-sh              zstdcat
 git                                  kmodsign               ptx                                stdbuf                 zstdgrep
 git-receive-pack                     landscape-sysinfo      pwd                                strace                 zstdless
 git-shell                            ld                     pwdx                               strace-log-merge       zstdmt
 git-upload-archive                   ld.bfd                 py3clean                           streamzip
 git-upload-pack                      ld.so                  py3compile                         strings

/boot:
System.map-7.0.0-1006-aws  efi   initrd.img                 initrd.img.old  microcode.cpio  vmlinuz-7.0.0-1006-aws
config-7.0.0-1006-aws      grub  initrd.img-7.0.0-1006-aws  lost+found      vmlinuz         vmlinuz.old

/dev:
autofs              dri            log           mem         port      stderr  tty16  tty27  tty38  tty49  tty6   ttyprintk    vcs5   vcsu3        zfs
block               ecryptfs       loop-control  mqueue      ppp       stdin   tty17  tty28  tty39  tty5   tty60  udmabuf      vcs6   vcsu4
btrfs-control       fb0            loop0         net         psaux     stdout  tty18  tty29  tty4   tty50  tty61  uhid         vcsa   vcsu5
char                fd             loop1         ng0n1       ptmx      tty     tty19  tty3   tty40  tty51  tty62  uinput       vcsa1  vcsu6
console             full           loop2         null        pts       tty0    tty2   tty30  tty41  tty52  tty63  urandom      vcsa2  vfio
core                fuse           loop3         nvme0       random    tty1    tty20  tty31  tty42  tty53  tty7   userfaultfd  vcsa3  vga_arbiter
cpu                 gpt-auto-root  loop4         nvme0n1     rfkill    tty10   tty21  tty32  tty43  tty54  tty8   userio       vcsa4  vhost-net
cpu_dma_latency     hpet           loop5         nvme0n1p1   root      tty11   tty22  tty33  tty44  tty55  tty9   vcs          vcsa5  vhost-vsock
cpu_wakeup_latency  hugepages      loop6         nvme0n1p13  rtc       tty12   tty23  tty34  tty45  tty56  ttyS0  vcs1         vcsa6  vmci
cuse                hwrng          loop7         nvme0n1p14  rtc0      tty13   tty24  tty35  tty46  tty57  ttyS1  vcs2         vcsu   vmclock0
disk                input          mapper        nvme0n1p15  shm       tty14   tty25  tty36  tty47  tty58  ttyS2  vcs3         vcsu1  vsock
dma_heap            kmsg           mcelog        nvram       snapshot  tty15   tty26  tty37  tty48  tty59  ttyS3  vcs4         vcsu2  zero

/etc:
ModemManager            cron.monthly    gnutls              ld.so.conf      modules                 plymouth      selinux            tmpfiles.d
PackageKit              cron.weekly     gprofng.rc          ld.so.conf.d    modules-load.d          pm            sensors.d          tpm2-tss
X11                     cron.yearly     groff               ldap            mtab                    polkit-1      sensors3.conf      ubuntu-advantage
acpi                    crontab         group               legal           multipath               pollinate     services           ucf.conf
adduser.conf            crypttab        group-              libaudit.conf   multipath.conf          ppp           sgml               udev
alternatives            dbus-1          grub.d              libblockdev     nanorc                  profile       shadow             udisks2
apparmor                debconf.conf    gshadow             libibverbs.d    needrestart             profile.d     shadow-            ufw
apparmor.d              debian_version  gshadow-            libnl-3         netconfig               protocols     shells             update-manager
apport                  debuginfod      gss                 locale.conf     netplan                 python3       skel               update-motd.d
apt                     default         hdparm.conf         locale.gen      network                 python3.14    sos                update-notifier
bash.bashrc             deluser.conf    hibinit-config.cfg  localtime       networkd-dispatcher     rc0.d         ssh                usb_modeswitch.conf
bash_completion         depmod.d        host.conf           logcheck        networks                rc1.d         ssl                usb_modeswitch.d
bash_completion.d       dhcp            hostname            login.defs      newt                    rc2.d         subgid             vconsole.conf
bindresvport.blacklist  dhcpcd.conf     hosts               logrotate.conf  nftables.conf           rc3.d         subgid-            vim
binfmt.d                dpkg            hosts.allow         logrotate.d     nsswitch.conf           rc4.d         subuid             vmware-tools
ca-certificates         dracut.conf     hosts.deny          lsb-release     opt                     rc5.d         subuid-            vtrgb
ca-certificates.conf    dracut.conf.d   init.d              lvm             os-release              rc6.d         sudo.conf          wgetrc
chrony                  e2scrub.conf    initramfs-tools     machine-id      overlayroot.conf        rcS.d         sudo_logsrvd.conf  xattr.conf
cloud                   ec2_version     inputrc             magic           overlayroot.local.conf  resolv.conf   sudoers            xdg
console-setup           environment     iscsi               magic.mime      pam.conf                rmt           sudoers.d          xml
credstore               ethertypes      issue               manpath.config  pam.d                   rpc           supercat           zsh_command_not_found
credstore.encrypted     fstab           issue.net           mdadm           passwd                  rsyslog.conf  sysctl.d
cron.d                  fuse.conf       kernel              mime.types      passwd-                 rsyslog.d     sysstat
cron.daily              fwupd           landscape           mke2fs.conf     perl                    screenrc      systemd
cron.hourly             gai.conf        ld.so.cache         modprobe.d      pki                     security      terminfo

/home:
ubuntu

/lib:
NetworkManager     dracut             kernel                                man-db               pam.d                sysctl.d
apparmor           ec2-hibinit-agent  klibc                                 mime                 pcrlock.d            systemd
apt                environment.d      klibc-vJ92VccDdUm9RkZ29z4hx5GyxAs.so  modprobe.d           pm-utils             sysusers.d
binfmt.d           file               libmpathcmd.so.0                      modules              policykit-1          tmpfiles.d
cargo              finalrd            libmpathpersist.so.0                  modules-load.d       polkit-1             ubuntu-advantage
cloud-init         firmware           libmpathutil.so.0                     multipath            python3              ubuntu-release-upgrader
cnf-update-db      git-core           libmultipath.so.0                     nagios               python3.14           udev
command-not-found  gnupg              libperf-jvmti.so                      needrestart          recovery-mode        udisks2
compat-ld          gnupg2             linux                                 netplan              rsyslog              ufw
console-setup      groff              linux-aws-tools-7.0.0-1006            networkd-dispatcher  sasl2                update-notifier
cryptsetup         grub               linux-boot-probes                     nvpcr                sftp-server          valgrind
dbus-1.0           hdparm             linux-tools                           open-iscsi           shim                 x86_64-linux-gnu
depmod.d           init               llvm-21                               openssh              snapd
dhcpcd             initcpio           locale                                os-probes            software-properties
dpkg               initramfs-tools    lsb                                   os-release           ssl

/lib64:
ld-linux-x86-64.so.2
ls: cannot open directory '/lost+found': Permission denied

/media:

/mnt:

/opt:

/proc:
1     148   20    2405  28   38  49   58   654  70   888         devices        ioports        loadavg       pressure       thread-self
10    15    202   2478  29   39  5    59   66   734  906         diskstats      irq            locks         schedstat      timer_list
1017  16    203   2479  294  4   50   596  662  738  acpi        dma            kallsyms       mdstat        scsi           tty
1078  1651  2093  25    295  40  51   6    663  743  bootconfig  driver         kcore          meminfo       self           uptime
1080  17    2095  2520  3    41  52   60   664  783  buddyinfo   dynamic_debug  key-users      misc          slabinfo       version
117   179   21    2524  30   42  53   61   669  8    bus         execdomains    keys           modules       softirqs       version_signature
12    18    2100  257   31   43  533  62   67   81   cgroups     fb             kmsg           mounts        stat           vmallocinfo
129   19    22    260   32   44  54   63   671  812  cmdline     filesystems    kpagecgroup    mtrr          swaps          vmstat
13    195   23    2602  33   46  55   65   672  82   consoles    fs             kpagecount     net           sys            zoneinfo
14    197   24    27    34   47  56   652  68   83   cpuinfo     interrupts     kpageflags     pagetypeinfo  sysrq-trigger
146   2     2403  271   36   48  57   653  7    851  crypto      iomem          latency_stats  partitions    sysvipc
ls: cannot open directory '/root': Permission denied

/run:
acpid.pid      cloud-init     cryptsetup       irqbalance            machine-id    multipathd.pid     setrans            sshd        tpm2-tss
acpid.socket   console-setup  dbus             lock                  media         multipathd.socket  shm                sshd.pid    udev
agetty.reload  credentials    dhcpcd           log                   motd.dynamic  polkit             snapd-snap.socket  sudo        udisks2
blkid          crond.pid      dmeventd-client  lvm                   mount         screen             snapd.socket       systemd     user
chrony         crond.reboot   dmeventd-server  lxd-installer.socket  multipath     sendsigs.omit.d    ssh-unix-local     tmpfiles.d  uuidd

/sbin:
ModemManager           dpkg-preconfigure     integritysetup               mkfs.vfat              rtacct                undump.bt
aa-load                dpkg-reconfigure      invoke-rc.d                  mkfs.xfs               rtcwake               unix_chkpwd
aa-remove-unknown      dpll                  ip                           mkhomedir_helper       rtmon                 unix_update
aa-status              drsnoop-bpfcc         ip6tables                    mkinitramfs            rubycalls-bpfcc       uobjnew
aa-teardown            dump.exfat            ip6tables-apply              mklost+found           rubyflow-bpfcc        update-ca-certificates
accessdb               dumpe2fs              ip6tables-legacy             mkntfs                 rubygc-bpfcc          update-catalog
acpid                  e2freefrag            ip6tables-legacy-restore     mkswap                 rubyobjnew-bpfcc      update-grub
add-shell              e2fsck                ip6tables-legacy-save        modinfo                rubystat-bpfcc        update-grub-gfxpayload
addgnupghome           e2image               ip6tables-nft                modprobe               runqlat-bpfcc         update-grub2
addgroup               e2label               ip6tables-nft-restore        mount.fuse             runqlat.bt            update-ieee-data
adduser                e2mmpstatus           ip6tables-nft-save           mount.fuse3            runqlen-bpfcc         update-info-dir
agetty                 e2scrub               ip6tables-restore            mount.lowntfs-3g       runqlen.bt            update-initramfs
apparmor_parser        e2scrub_all           ip6tables-restore-translate  mount.ntfs             runqslower-bpfcc      update-locale
apparmor_status        e2undo                ip6tables-save               mount.ntfs-3g          runuser               update-passwd
applygnupgdefaults     e4crypt               ip6tables-translate          mountsnoop-bpfcc       service               update-pciids
argdist-bpfcc          e4defrag              iptables                     mpathpersist           setcap                update-rc.d
arpd                   ebtables              iptables-apply               mptcpify-bpfcc         setuids.bt            update-secureboot-policy
arptables              ebtables-nft          iptables-legacy              multipath              setvesablank          update-shells
arptables-nft          ebtables-nft-restore  iptables-legacy-restore      multipathc             setvtrgb              update-xmlcatalog
arptables-nft-restore  ebtables-nft-save     iptables-legacy-save         multipathd             sfdisk                usb_modeswitch
arptables-nft-save     ebtables-restore      iptables-nft                 mysqld_qslower-bpfcc   sgdisk                usb_modeswitch_dispatcher
arptables-restore      ebtables-save         iptables-nft-restore         naptime.bt             shadowconfig          useradd
arptables-save         ebtables-translate    iptables-nft-save            needrestart            shmsnoop-bpfcc        userdel
arptables-translate    era_check             iptables-restore             netplan                shutdown              usermod
badblocks              era_dump              iptables-restore-translate   netqtop-bpfcc          slabratetop-bpfcc     ustat
bashreadline-bpfcc     era_invalidate        iptables-save                newusers               sofdsnoop-bpfcc       uthreads
bashreadline.bt        era_restore           iptables-translate           nfnl_osf               softirqs-bpfcc        uuidd
bcache-super-show      ethtool               irqbalance                   nfsdist-bpfcc          solisten-bpfcc        validlocale
bindsnoop-bpfcc        execsnoop-bpfcc       irqbalance-ui                nfsslower-bpfcc        sshd                  vcstime
biolatency-bpfcc       execsnoop.bt          iscsi-iname                  nft                    ssllatency.bt         vdpa
biolatency-kp.bt       exfat2img             iscsi_discovery              nodegc-bpfcc           sslsniff-bpfcc        veritysetup
biolatency.bt          exfatlabel            iscsiadm                     nodestat-bpfcc         sslsnoop.bt           vfscount-bpfcc
biolatpcts-bpfcc       exitsnoop-bpfcc       iscsid                       nologin                stackcount-bpfcc      vfscount.bt
biopattern-bpfcc       ext4dist-bpfcc        iscsistart                   ntfsclone              start-stop-daemon     vfsstat-bpfcc
biosdecode             ext4slower-bpfcc      iucode-tool                  ntfscp                 statsnoop-bpfcc       vfsstat.bt
biosnoop-bpfcc         f2fsslower-bpfcc      iucode_tool                  ntfslabel              statsnoop.bt          vgcfgbackup
biosnoop.bt            faillock              javacalls-bpfcc              ntfsresize             sudo_logsrvd          vgcfgrestore
biostacks.bt           fatlabel              javaflow-bpfcc               ntfsundelete           sudo_sendlog.ws       vgchange
biotop-bpfcc           fdisk                 javagc-bpfcc                 numasched-bpfcc        sulogin               vgck
bitesize-bpfcc         filefrag              javaobjnew-bpfcc             offcputime-bpfcc       swapin.bt             vgconvert
bitesize.bt            filegone-bpfcc        javastat-bpfcc               offwaketime-bpfcc      swaplabel             vgcreate
blkdeactivate          filelife-bpfcc        javathreads-bpfcc            on_ac_power            swapoff               vgdisplay
blkdiscard             fileslower-bpfcc      kbdrate                      oomkill-bpfcc          swapon                vgexport
blkid                  filetop-bpfcc         killall5                     oomkill.bt             syncsnoop-bpfcc       vgextend
blkpr                  findfs                killsnoop-bpfcc              opensnoop-bpfcc        syncsnoop.bt          vgimport
blockdev               fixparts              killsnoop.bt                 opensnoop.bt           syscount-bpfcc        vgimportclone
bpflist-bpfcc          fsadm                 klockstat-bpfcc              overlayroot-chroot     syscount.bt           vgmerge
bpftool                fsck                  kpartx                       ownership              sysctl                vgmknodes
bridge                 fsck.btrfs            kvmexit-bpfcc                pam-auth-update        tarcat                vgreduce
btrfsdist-bpfcc        fsck.cramfs           ldconfig                     pam_extrausers_chkpwd  tc                    vgremove
btrfsslower-bpfcc      fsck.exfat            llcstat-bpfcc                pam_extrausers_update  tclcalls-bpfcc        vgrename
cache_check            fsck.ext2             loads.bt                     pam_getenv             tclflow-bpfcc         vgs
cache_dump             fsck.ext3             locale-gen                   pam_namespace_helper   tclobjnew-bpfcc       vgscan
cache_metadata_size    fsck.ext4             logrotate                    pam_timestamp_check    tclstat-bpfcc         vgsplit
cache_repair           fsck.fat              logsave                      parted                 tcpaccept-bpfcc       vigr
cache_restore          fsck.minix            losetup                      partprobe              tcpaccept.bt          vipw
cache_writeback        fsck.msdos            lsmod                        pdata_tools            tcpcong-bpfcc         virtiostat-bpfcc
cachestat-bpfcc        fsck.vfat             luksformat                   perlcalls-bpfcc        tcpconnect-bpfcc      visudo
cachetop-bpfcc         fsck.xfs              lvchange                     perlflow-bpfcc         tcpconnect.bt         visudo.ws
capable-bpfcc          fsfreeze              lvconvert                    perlstat-bpfcc         tcpconnlat-bpfcc      vpddecode
capable.bt             fstab-decode          lvcreate                     phpcalls-bpfcc         tcpdrop-bpfcc         wakeuptime-bpfcc
capsh                  fstrim                lvdisplay                    phpflow-bpfcc          tcpdrop.bt            wipefs
cfdisk                 funccount-bpfcc       lvextend                     phpstat-bpfcc          tcplife-bpfcc         wqlat-bpfcc
cgdisk                 funcinterval-bpfcc    lvm                          pidpersec-bpfcc        tcplife.bt            writeback.bt
chgpasswd              funclatency-bpfcc     lvmconfig                    pidpersec.bt           tcpretrans-bpfcc      xfs_admin
chpasswd               funcslower-bpfcc      lvmdiskscan                  plymouthd              tcpretrans.bt         xfs_bmap
chronyd                gdisk                 lvmdump                      poweroff               tcprtt-bpfcc          xfs_copy
cobjnew-bpfcc          genl                  lvmpolld                     ppchcalls-bpfcc        tcpstates-bpfcc       xfs_db
compactsnoop-bpfcc     getcap                lvmsadc                      profile-bpfcc          tcpsubnet-bpfcc       xfs_estimate
cpudist-bpfcc          gethostlatency-bpfcc  lvmsar                       pvchange               tcpsynbl-bpfcc        xfs_freeze
cpuunclaimed-bpfcc     gethostlatency.bt     lvreduce                     pvck                   tcpsynbl.bt           xfs_fsr
cpuwalk.bt             getpcaps              lvremove                     pvcreate               tcptop-bpfcc          xfs_growfs
criticalstat-bpfcc     getty                 lvrename                     pvdisplay              tcptracer-bpfcc       xfs_info
cron                   gnuchroot             lvresize                     pvmove                 thin_check            xfs_io
cryptdisks_start       groupadd              lvs                          pvremove               thin_delta            xfs_logprint
cryptdisks_stop        groupdel              lvscan                       pvresize               thin_dump             xfs_mdrestore
cryptsetup             groupmod              lxc                          pvs                    thin_ls               xfs_metadump
ctrlaltdel             grpck                 lxd                          pvscan                 thin_metadata_pack    xfs_mkfile
dbslower-bpfcc         grpconv               make-bcache                  pwck                   thin_metadata_size    xfs_ncheck
dbstat-bpfcc           grpunconv             mdadm                        pwconv                 thin_metadata_unpack  xfs_property
dcb                    grub-bios-setup       mdflush-bpfcc                pwhistory_helper       thin_migrate          xfs_protofile
dcsnoop-bpfcc          grub-install          mdflush.bt                   pwunconv               thin_repair           xfs_quota
dcsnoop.bt             grub-macbless         mdmon                        pythoncalls-bpfcc      thin_restore          xfs_repair
dcstat-bpfcc           grub-mkconfig         memleak-bpfcc                pythonflow-bpfcc       thin_rmap             xfs_rtcp
deadlock-bpfcc         grub-mkdevicemap      mkdosfs                      pythongc-bpfcc         thin_trim             xfs_scrub
debugfs                grub-probe            mke2fs                       pythonstat-bpfcc       threadsnoop-bpfcc     xfs_scrub_all
delgroup               grub-reboot           mkfs                         rdmaucma-bpfcc         threadsnoop.bt        xfs_spaceman
deluser                grub-set-default      mkfs.bfs                     readahead-bpfcc        tipc                  xfsdist-bpfcc
depmod                 halt                  mkfs.btrfs                   readprofile            tplist-bpfcc          xfsdist.bt
devlink                hardirqs-bpfcc        mkfs.cramfs                  reboot                 trace-bpfcc           xfsslower-bpfcc
dhcpcd                 hdparm                mkfs.exfat                   remove-shell           ttysnoop-bpfcc        xtables-legacy-multi
dirtop-bpfcc           hwclock               mkfs.ext2                    reset-trace-bpfcc      tune.exfat            xtables-monitor
dmeventd               iconvconfig           mkfs.ext3                    resize2fs              tune2fs               xtables-nft-multi
dmidecode              init                  mkfs.ext4                    resolvconf             ucalls                zerofree
dmsetup                inject-bpfcc          mkfs.fat                     rmmod                  uflow                 zfsdist-bpfcc
dmstats                insmod                mkfs.minix                   rmt                    ufw                   zfsslower-bpfcc
dosfsck                install-sgmlcatalog   mkfs.msdos                   rmt-tar                ugc                   zic
dosfslabel             installkernel         mkfs.ntfs                    rsyslogd               umount.udisks2        zramctl

/snap:
README  amazon-ssm-agent  bin  core22  snapd

/srv:

/sys:
block  bus  class  dev  devices  firmware  fs  hypervisor  kernel  module  power

/tmp:
snap-private-tmp                                                              systemd-private-bc68f90e3f3b4b1d9b029c495053bc72-irqbalance.service-q3i2G3
systemd-private-bc68f90e3f3b4b1d9b029c495053bc72-ModemManager.service-sfTzSI  systemd-private-bc68f90e3f3b4b1d9b029c495053bc72-polkit.service-M8gaFB
systemd-private-bc68f90e3f3b4b1d9b029c495053bc72-chrony.service-roGwUO        systemd-private-bc68f90e3f3b4b1d9b029c495053bc72-systemd-logind.service-RxhMS3

/usr:
bin  games  include  lib  lib64  libexec  local  sbin  share  src

/var:
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


## 🧾 Server Baseline

| Item | Result|
|------|-------|
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
