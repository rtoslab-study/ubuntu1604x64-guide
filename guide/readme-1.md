# ������Ubuntu 16.04 X64 LTS���������׼��(1)

����ʱ�䣺2021-08-21

## һ��������Ϣ

### 1����������

```
VMware-workstation-full-15.5.6-16341506.exe
```

### 2����װ����

```
ubuntu-16.04.7-desktop-amd64.iso
```

### 3���û���/����

```
skyhigh/highsky
```

### 4�����ڸ���Դ��Ϣ

���������ݴ�Ϊsources.list������ʹ��UltraISO�����̾���ʽ����

```
# Ĭ��ע����Դ�뾵������� apt update �ٶȣ�������Ҫ������ȡ��ע��
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

# Ԥ�������Դ������������
# deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
```

## ����ϵͳ��װ

### 1�����������

![](./_pics_/vm-01.png)

![](./_pics_/vm-02.png)

![](./_pics_/vm-03.png)

![](./_pics_/vm-04.png)

![](./_pics_/vm-05.png)

![](./_pics_/vm-06.png)

![](./_pics_/vm-07.png)

![](./_pics_/vm-08.png)

![](./_pics_/vm-09.png)

![](./_pics_/vm-10.png)

![](./_pics_/vm-11.png)

![](./_pics_/vm-12.png)

![](./_pics_/vm-13.png)

### 2�����������Ӳ��

![](./_pics_/vm-14.png)

![](./_pics_/vm-15.png)

![](./_pics_/vm-16.png)

![](./_pics_/vm-17.png)

![](./_pics_/vm-18.png)

![](./_pics_/vm-19.png)

### 3��Ubuntu��װ

![](./_pics_/ubuntu-01.png)

![](./_pics_/ubuntu-02.png)

![](./_pics_/ubuntu-03.png)

![](./_pics_/ubuntu-04.png)

![](./_pics_/ubuntu-05.png)

![](./_pics_/ubuntu-06.png)

![](./_pics_/ubuntu-07.png)

![](./_pics_/ubuntu-08.png)

![](./_pics_/ubuntu-09.png)

![](./_pics_/ubuntu-10.png)

![](./_pics_/ubuntu-11.png)

## ����ϵͳ����

### 1��������Դ��ַ������

```
sudo mv /etc/apt/source.list /etc/apt/source.list.old
sudo cp source.list /etc/apt
sudo chmod 664 /etc/apt/source.list

sudo apt-get update
sudo apt-get upgrade
```

### 2����װVMware Tools

![](./_pics_/vmtools-01.png)

![](./_pics_/vmtools-02.png)

![](./_pics_/vmtools-03.png)

![](./_pics_/vmtools-04.png)

![](./_pics_/vmtools-05.png)

![](./_pics_/vmtools-06.png)

![](./_pics_/vmtools-07.png)

### 3������dashΪbash

��߽ű�������

```
sudo dpkg-reconfigure dash
```

![](./_pics_/bash-01.png)

### 4������i386�ܹ�֧��

����32λ���л���

```
sudo dpkg --add-architecture i386
sudo apt-get update
```

