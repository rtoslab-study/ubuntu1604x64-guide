# ������Ubuntu 16.04 X64 LTS���������׼��(2)

����ʱ�䣺2021-08-21

### 5����װ�����

C#����(֧��Ŀǰ����qmake��sdk����)

```
sudo apt-get install flex
sudo apt-get install bison
sudo apt-get install mono-complete
```

Linux�ں˱���

```
sudo apt-get install libncurses5-dev
sudo apt-get install libssl-dev
```

WindRiver������������

```
sudo apt-get install libstdc++6:i386 libgtk2.0-0:i386 libxtst6:i386 libxt6:i386
sudo apt-get install gtk2-engines-murrine:i386 libcanberra-gtk-module:i386 unity-gtk2-module:i386
sudo apt-get install overlay-scrollbar-gtk2:i386 libatk-adaptor:i386 libgail-common:i386
sudo apt-get install libpangox-1.0-0:i386 libpangoxft-1.0-0:i386
sudo apt-get install gvfs-backends:i386 libsmbclient:i386 samba-libs:i386 python-talloc:i386
```

Yocto��������

```
sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib build-essential chrpath socat libsdl1.2-dev
```

Yocto i.MX����

```
sudo apt-get install libsdl1.2-dev xterm sed cvs subversion coreutils texi2html docbook-utils python-pysqlite2 help2man make gcc g++ desktop-file-utils libgl1-mesa-dev libglu1-mesa-dev mercurial autoconf automake groff curl lzop asciidoc u-boot-tools
```

openssh-server(SSH����)

```
sudo apt-get install openssh-server
```

lftp(sftp�����пͻ���)

```
sudo apt-get install lftp
```

filezilla(ftpͼ�ν���ͻ���)

```
sudo apt-get install filezilla
```

privoxy(socks5����ת��)

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

socat(����"Yocto��������"��װ��Ϊgit�Ĵ����ṩ֧��)

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

���git������

```
git config --global core.gitproxy gitproxy
git config --global --unset core.gitproxy
```

xutils-dev

```
sudo apt-get install xutils-dev
```

cloc(������ͳ��)

```
sudo apt-get install cloc
```

binwalk(�������ļ�����)

```
sudo apt-get install binwalk
```

gimp(ͼƬ������ͼƬ����ΪC����Դ���ļ�)

```
sudo apt-get install gimp
```

isomaster(���̾����ļ�����)

```
sudo apt-get install isomaster
```

xmake(���빤����֯���ߣ�v2.5.6)

```
bash <(curl -fsSL https://xmake.io/shget.text)
```

cgdb(gdb�ַ�ģʽǰ��)

```
sudo apt-get install libreadline-dev
git clone git://github.com/cgdb/cgdb.git
cd cgdb/
./autogen.sh
./configure
make
sudo make install
```

mingw-w64(windows���湤����)

```
sudo apt-get install mingw-w64
```

docker-ce(������������)

```
sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```bash
sudo add-apt-repository \
   "deb [arch=amd64] https://mirrors.tuna.tsinghua.edu.cn/docker-ce/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

```
sudo apt-get update
sudo apt-get install docker-ce
sudo apt-get install docker-compose
```

SecureCRT & SecureFX

```
cd ~/TOOLS/scrt-sfx-8.7.3
sudo ./SecureCRT
sudo ./SecureFX
```

