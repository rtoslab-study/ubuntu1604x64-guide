# ������Ubuntu 16.04 X64 LTS���������׼��(2)

����ʱ�䣺2021-10-09

### 5����װ�����

C#����(֧��Ŀǰ����qmake��sdk����)

```
sudo apt-get install flex
sudo apt-get install bison
sudo apt-get install mono-complete
```

#### Linux�ں˱���

```
sudo apt-get install libncurses5-dev
sudo apt-get install libssl-dev
```

#### WindRiver������������

```
sudo apt-get install libstdc++6:i386 libgtk2.0-0:i386 libxtst6:i386 libxt6:i386
sudo apt-get install gtk2-engines-murrine:i386 libcanberra-gtk-module:i386 unity-gtk2-module:i386
sudo apt-get install overlay-scrollbar-gtk2:i386 libatk-adaptor:i386 libgail-common:i386
sudo apt-get install libpangox-1.0-0:i386 libpangoxft-1.0-0:i386
sudo apt-get install gvfs-backends:i386 libsmbclient:i386 samba-libs:i386 python-talloc:i386
```

#### Yocto��������

```
sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib build-essential chrpath socat libsdl1.2-dev
```

#### Yocto i.MX����

```
sudo apt-get install libsdl1.2-dev xterm sed cvs subversion coreutils texi2html docbook-utils python-pysqlite2 help2man make gcc g++ desktop-file-utils libgl1-mesa-dev libglu1-mesa-dev mercurial autoconf automake groff curl lzop asciidoc u-boot-tools
```

#### openssh-server(SSH����)

```
sudo apt-get install openssh-server
```

#### lftp(sftp�����пͻ���)

```
sudo apt-get install lftp
```

#### filezilla(ftpͼ�ν���ͻ���)

```
sudo apt-get install filezilla
```

#### privoxy(socks5����ת��)

```
sudo apt-get install privoxy
sudo gedit /etc/privoxy/config
```

```
listen-address 127.0.0.1:10809
forward-socks5 / 127.0.0.1:10808 .
```

```
sudo /etc/init.d/privoxy start
sudo /etc/init.d/privoxy restart
```

#### socat(����"Yocto��������"��װ��Ϊgit�Ĵ����ṩ֧��)

```
sudo apt-get install socat
sudo gedit /usr/bin/gitproxy
```

```
#!/bin/bash
PROXY=127.0.0.1
PROXYPORT=10809
exec socat STDIO PROXY:$PROXY:$1:$2,proxyport=$PROXYPORT
```

```
sudo  chmod +x /usr/bin/gitproxy
```

#### ���git������

```
git config --global core.gitproxy gitproxy
git config --global --unset core.gitproxy
```

#### xutils-dev

```
sudo apt-get install xutils-dev
```

#### cloc(������ͳ��)

```
sudo apt-get install cloc
```

#### binwalk(�������ļ�����)

```
sudo apt-get install binwalk
```

#### gimp(ͼƬ������ͼƬ����ΪC����Դ���ļ�)

```
sudo apt-get install gimp
```

#### isomaster(���̾����ļ�����)

```
sudo apt-get install isomaster
```

#### xmake(���빤����֯���ߣ�v2.5.8)

```
bash <(curl -fsSL https://xmake.io/shget.text)
xmake update
```

#### cgdb(gdb�ַ�ģʽǰ�ˣ����Ҫ��gdb 7.2)

```
sudo apt-get install libreadline-dev
git clone git://github.com/cgdb/cgdb.git
cd cgdb/
./autogen.sh
./configure
make
sudo make install
```

#### mingw-w64(windows���湤����)

```
sudo apt-get install mingw-w64
```

#### docker-ce(������������)

```
sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```bash
sudo add-apt-repository \
   "deb [arch=amd64] https://mirrors.aliyun.com/docker-ce/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

```
sudo apt-get update
sudo apt-get install docker-ce
sudo apt-get install docker-compose
```

#### SecureCRT & SecureFX

```
cd ~/TOOLS/scrt-sfx-8.7.3
sudo ./SecureCRT
sudo ./SecureFX
```

#### clang-format(�����ʽ������)

```
sudo apt-get install clang-format
```

#### fluxcomp(DirectFB����)

```
sudo tar -Jxf flux_bin.tar.xz -C /opt/
```

#### gcc-4.4.0-pmon(��оPMON���빤����)

```
sudo tar -xf gcc-4.4.0-pmon.tgz -C /opt/
```

#### gcc-4.4-gnu_pmon(��оPMON���빤����)

```
sudo tar -xf gcc-4.4-gnu_pmon.tar.gz -C /
```

#### gcc-4.4.7-7215-n64-loongson(��оUEFI���빤����)

```
sudo tar -xf gcc-4.4.7-7215-n64-loongson.tar.gz -C /opt/
```

#### ejtag-debug-v3.25.19(��оejtag���Թ���)

```
tar -xf ejtag-debug-v3.25.19.tar.gz
```

#### linux-headers-4.15.0-106(haps-x86Ŀ����ͷ�ļ�)

```
sudo apt-get install linux-headers-4.15.0-106 linux-headers-4.15.0-106-generic
```

#### samba(��windows�����ļ�)

```
sudo apt-get install samba
sudo apt-get install smbclient
```

�޸�/etc/samba/smb.conf����ĩβ����

```
[sambashare]
        comment = Samba on Ubuntu
        path = /home/skyhigh/WORK
        readonly = no
        browsable = yes
```

����smb�û�(��Ҫϵͳ�������û�)��������ʾ��������

```
sudo smbpasswd -a skyhigh
```

ʹ�ÿͻ��˲��ԣ�����ʾ��������

```
smbclient -L 192.168.22.128
```

Windows�˵�����

![](./_pics_/smb-win10-01.png)

![](./_pics_/smb-win10-02.png)

![](./_pics_/smb-win10-03.png)

#### cmake(���빤��)

```
./bootstrap -- -DCMAKE_BUILD_TYPE:STRING=Release
make
sudo make install
```

#### gdb(���Թ��ߣ�֧�ֶ�CPU�ܹ���֧��TUI�������cgdb)

```
cd WORK
mkdir -p gdb/build
mkdir -p gdb/install
tar xf gdb-9.2.tar.gz
cd gdb/build/
../../gdb-9.2/configure --enable-targets=all --enable-64-bit-bfd --enable-tui=yes --prefix=/home/skyhigh/WORK/gdb/install
make
make install
```

```
export PATH=$HOME/WORK/gdb/install/bin:$PATH
cgdb
```

#### vim(����༭����)

```
sudo apt-get install vim
```

