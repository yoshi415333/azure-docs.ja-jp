---
title: GPT パーティションがある OS ディスクのサイズを変更する |Microsoft Docs
description: この記事では、GPT パーティションがある OS ディスクのサイズを変更する手順について説明します。
services: virtual-machines-linux
documentationcenter: ''
author: kailashmsft
manager: dcscontentpm
editor: ''
tags: ''
ms.service: security
ms.topic: troubleshooting
ms.workload: infrastructure-services
ms.devlang: azurecli
ms.date: 05/03/2020
ms.author: kaib
ms.custom: seodec18
ms.openlocfilehash: 7c408e8e29b3f9ac423a6104c40242f11f93a171
ms.sourcegitcommit: fdec8e8bdbddcce5b7a0c4ffc6842154220c8b90
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2020
ms.locfileid: "83651092"
---
# <a name="resize-an-os-disk-that-has-a-gpt-partition"></a>GPT パーティションがある OS ディスクのサイズを変更する

> [!NOTE]
> このシナリオは、GUID パーティション テーブル (GPT) パーティションを持つ OS ディスクにのみ適用されます。

この記事では、Linux で GPT パーティションを含む OS ディスクのサイズを増やす方法について説明します。 

## <a name="identify-whether-the-os-disk-has-an-mbr-or-gpt-partition"></a>OS ディスクに MBR または GPT パーティションがあるかどうかを確認する

**parted** コマンドを使用して、ディスク パーティションがマスター ブート レコード (MBR) パーティションまたは GPT パーティションのどちらで作成されているかを特定します。

### <a name="mbr-partition"></a>MBR パーティション

次の出力では、**Partition Table** に **msdos** の値が示されています。 この値は、MBR パーティションを識別します。

```
[user@myvm ~]# parted -l /dev/sda
Model: Msft Virtual Disk (scsi)
Disk /dev/sda: 107GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos
Number  Start   End     Size    Type     File system  Flags
1       1049kB  525MB   524MB   primary  ext4         boot
2       525MB   34.4GB  33.8GB  primary  ext4
[user@myvm ~]#
```

### <a name="gpt-partition"></a>GPT パーティション

次の出力では、**Partition Table** に **gpt** の値が示されています。 この値は、GPT パーティションを識別します。

```
[user@myvm ~]# parted -l /dev/sda
Model: Msft Virtual Disk (scsi)
Disk /dev/sda: 68.7GB
Sector size (logical/physical): 512B/512B
Partition Table: gpt
Disk Flags:

Number  Start   End     Size    File system  Name                  Flags
1       1049kB  525MB   524MB   fat16        EFI System Partition  boot
2       525MB   1050MB  524MB   xfs
3       1050MB  1052MB  2097kB                                     bios_grub
4       1052MB  68.7GB  67.7GB                                     lvm
```

仮想マシン (VM) の OS ディスク上に GPT パーティションがある場合、OS ディスクのサイズを増やします。

## <a name="increase-the-size-of-the-os-disk"></a>OS ディスクのサイズを増やす

次の手順は、Linux での動作保証済みディストリビューションに適用されます。

> [!NOTE]
> 続行する前に、VM のバックアップ コピーを作成するか、OS ディスクのスナップショットを取得してください。

### <a name="ubuntu"></a>Ubuntu

Ubuntu 16.x および 18.x で OS ディスクのサイズを増やすには、次の操作を実行します。

1. VM を停止します。
1. ポータルから OS ディスクのサイズを増やします。
1. VM を再起動し、**root** ユーザーとして VM にログインします。
1. OS ディスクに増加したファイル システム サイズが表示されていることを確認します。

次の例に示すように、ポータルから OS ディスクのサイズが 100 GB に変更されています。 **/** にマウントされた **/dev/sda1** ファイル システムには 97 GB と表示されます。

```
user@myvm:~# df -Th
Filesystem     Type      Size  Used Avail Use% Mounted on
udev           devtmpfs  314M     0  314M   0% /dev
tmpfs          tmpfs      65M  2.3M   63M   4% /run
/dev/sda1      ext4       97G  1.8G   95G   2% /
tmpfs          tmpfs     324M     0  324M   0% /dev/shm
tmpfs          tmpfs     5.0M     0  5.0M   0% /run/lock
tmpfs          tmpfs     324M     0  324M   0% /sys/fs/cgroup
/dev/sda15     vfat      105M  3.6M  101M   4% /boot/efi
/dev/sdb1      ext4       20G   44M   19G   1% /mnt
tmpfs          tmpfs      65M     0   65M   0% /run/user/1000
user@myvm:~#
```

### <a name="suse"></a>SUSE

Suse 12 SP4、SUSE SLES 12 for SAP、SUSE SLES 15、および SUSE SLES 15 for SAP で OS ディスクのサイズを増やすには、次の操作を実行します。

1. VM を停止します。
1. ポータルから OS ディスクのサイズを増やします。
1. VM を再起動します。

VM が再起動されたら、次の手順を実行します。

   1. 次のコマンドを使用して、**ルート** ユーザーとして VM にアクセスします。
   
      `#sudo su`

   1. 次のコマンドを使用して **gptfdisk** パッケージをインストールします。これは、OS ディスクのサイズを増やすために必要です。

      `#zypper install gptfdisk -y`

   1. ディスクで使用可能な最大セクターを表示するには、次のコマンドを実行します。

      `#sgdisk -e /dev/sda`

   1. 次のコマンドを使用して、パーティションを削除せずにサイズを変更します。 **parted** コマンドには **resizepart** という名前のオプションがあり、パーティションを削除せずにサイズを変更できます。 **resizepart** の後の 4 の数字は、4 番目のパーティションのサイズを変更することを示しています。

      `#parted -s /dev/sda "resizepart 4 -1" quit`

   1. **#lsblk** コマンドを実行して、パーティションが増加したかどうかを確認します。

      次の出力は、 **/dev/sda4** パーティションのサイズが 98.5 GB に変更されたことを示します。

      ```
      user@myvm:~ # lsblk
      NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
      sda      8:0    0  100G  0 disk
      ├─sda1   8:1    0    2M  0 part
      ├─sda2   8:2    0  512M  0 part /boot/efi
      └─sda4   8:4    0 98.5G  0 part /
      sdb      8:16   0   20G  0 disk
      └─sdb1   8:17   0   20G  0 part /mnt/resource
      ```
      
   1. 次のコマンドを使用して、OS ディスク上のファイル システムの種類を識別します。

      `blkid`

      出力例:

      ```
      #blkid

      user@myvm:~ # blkid
      /dev/sda1: PARTLABEL="p.legacy" PARTUUID="0122fd4c-0069-4a45-bfd4-98b97ccb6e8c"
      /dev/sda2: SEC_TYPE="msdos" LABEL_FATBOOT="EFI" LABEL="EFI" UUID="00A9-D170" TYPE="vfat" PARTLABEL="p.UEFI" PARTUUID="abac3cd8-949b-4e83-81b1-9636493388c7"
      /dev/sda3: LABEL="BOOT" UUID="aa2492db-f9ed-4f5a-822a-1233c06d57cc" TYPE="xfs" PARTLABEL="p.lxboot" PARTUUID="dfb36c61-b15f-4505-8e06-552cf1589cf7"
      /dev/sda4: LABEL="ROOT" UUID="26104965-251c-4e8d-b069-5f5323d2a9ba" TYPE="xfs" PARTLABEL="p.lxroot" PARTUUID="50fecee0-f22b-4406-94c3-622507e2dbce"
      /dev/sdb1: UUID="95239fce-ca97-4f03-a077-4e291588afc9" TYPE="ext4" PARTUUID="953afef3-01"
      ```

   1. ファイル システムの種類に基づいて、適切なコマンドを使用してファイル システムのサイズを変更します。

      **xfs** の場合、次のコマンドを使用します。

      ` #xfs_growfs /`

      出力例:

      ```
      user@myvm:~ # xfs_growfs /
      meta-data=/dev/sda4              isize=512    agcount=4, agsize=1867583 blks
               =                       sectsz=512   attr=2, projid32bit=1
               =                       crc=1        finobt=1 spinodes=0 rmapbt=0
               =                       reflink=0
      data     =                       bsize=4096   blocks=7470331, imaxpct=25
               =                       sunit=0      swidth=0 blks
      naming   =version 2              bsize=4096   ascii-ci=0 ftype=1
      log      =internal               bsize=4096   blocks=3647, version=2
               =                       sectsz=512   sunit=0 blks, lazy-count=1
      realtime =none                   extsz=4096   blocks=0, rtextents=0
      data blocks changed from 7470331 to 25820172
      ```

      **ext4** の場合、次のコマンドを使用します。

      ```#resize2fs /dev/sda4```

   1. 次のコマンドを使用して、**df-Th** のファイル システムの増加したサイズを確認します。

      `#df -Th`

      出力例:

      ```
      user@myvm:~ # df -Th
      Filesystem     Type      Size  Used Avail Use% Mounted on
      devtmpfs       devtmpfs  306M  4.0K  306M   1% /dev
      tmpfs          tmpfs     320M     0  320M   0% /dev/shm
      tmpfs          tmpfs     320M  8.8M  311M   3% /run
      tmpfs          tmpfs     320M     0  320M   0% /sys/fs/cgroup
      /dev/sda4      xfs        99G  1.8G   97G   2% /
      /dev/sda3      xfs      1014M   88M  927M   9% /boot
      /dev/sda2      vfat      512M  1.1M  511M   1% /boot/efi
      /dev/sdb1      ext4       20G   45M   19G   1% /mnt/resource
      tmpfs          tmpfs      64M     0   64M   0% /run/user/1000
      user@myvm:~ #
      ```

前の例では、OS ディスクのファイル システム サイズが増加していることがわかります。

### <a name="rhel"></a>RHEL

LVM で RHEL 7.x の OS ディスクのサイズを増やすには、次の操作を実行します。

1. VM を停止します。
1. ポータルから OS ディスクのサイズを増やします。
1. VM を起動します。

VM が再起動されたら、次の手順を実行します。

   1. 次のコマンドを使用して、**ルート** ユーザーとして VM にアクセスします。
   
      `#sudo su`

   1. **gptfdisk** パッケージをインストールします。これは、OS ディスクのサイズを増やすために必要です。

      `#yum install gdisk -y`

   1. ディスクで使用可能な最大セクターを表示するには、次のコマンドを実行します。

      `#sgdisk -e /dev/sda`

   1. 次のコマンドを使用して、パーティションを削除せずにサイズを変更します。 **parted** コマンドには **resizepart** という名前のオプションがあり、パーティションを削除せずにサイズを変更できます。 **resizepart** の後の 4 の数字は、4 番目のパーティションのサイズを変更することを示しています。

      `#parted -s /dev/sda "resizepart 4 -1" quit`
    
   1. 次のコマンドを実行して、パーティションが増加したことを確認します。

      `#lsblk`

      次の出力は、 **/dev/sda4** パーティションのサイズが 99 GB に変更されたことを示します。

      ```
      [user@myvm ~]# lsblk
      NAME              MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
      fd0                 2:0    1    4K  0 disk
      sda                 8:0    0  100G  0 disk
      ├─sda1              8:1    0  500M  0 part /boot/efi
      ├─sda2              8:2    0  500M  0 part /boot
      ├─sda3              8:3    0    2M  0 part
      └─sda4              8:4    0   99G  0 part
      ├─rootvg-tmplv    253:0    0    2G  0 lvm  /tmp
      ├─rootvg-usrlv    253:1    0   10G  0 lvm  /usr
      ├─rootvg-optlv    253:2    0    2G  0 lvm  /opt
      ├─rootvg-homelv   253:3    0    1G  0 lvm  /home
      ├─rootvg-varlv    253:4    0    8G  0 lvm  /var
      └─rootvg-rootlv   253:5    0    2G  0 lvm  /
      sdb                 8:16   0   50G  0 disk
      └─sdb1              8:17   0   50G  0 part /mnt/resource
      ```

   1. 次のコマンドを使用して、物理ボリューム (PV) のサイズを変更します。

      `#pvresize /dev/sda4`

      次の出力は、PV のサイズが 99.02 GB に変更されたことを示します。

      ```
      [user@myvm ~]# pvresize /dev/sda4
      Physical volume "/dev/sda4" changed
      1 physical volume(s) resized or updated / 0 physical volume(s) not resized

      [user@myvm ~]# pvs
      PV         VG     Fmt  Attr PSize   PFree
      /dev/sda4  rootvg lvm2 a--  <99.02g <74.02g
      ```

   1. 次の例では、次のコマンドを使用して、 **/dev/mapper/rootvg-rootlv** のサイズを 2 GB から 12 GB (10 GB の増加) に変更しています。 このコマンドでファイル システムのサイズも変更されます。

      `#lvresize -r -L +10G /dev/mapper/rootvg-rootlv`

      出力例:

      ```
      [user@myvm ~]# lvresize -r -L +10G /dev/mapper/rootvg-rootlv
      Size of logical volume rootvg/rootlv changed from 2.00 GiB (512 extents) to 12.00 GiB (3072 extents).
      Logical volume rootvg/rootlv successfully resized.
      meta-data=/dev/mapper/rootvg-rootlv isize=512    agcount=4, agsize=131072 blks
               =                       sectsz=4096  attr=2, projid32bit=1
               =                       crc=1        finobt=0 spinodes=0
      data     =                       bsize=4096   blocks=524288, imaxpct=25
               =                       sunit=0      swidth=0 blks
      naming   =version 2              bsize=4096   ascii-ci=0 ftype=1
      log      =internal               bsize=4096   blocks=2560, version=2
               =                       sectsz=4096  sunit=1 blks, lazy-count=1
      realtime =none                   extsz=4096   blocks=0, rtextents=0
      data blocks changed from 524288 to 3145728
      ```
         
   1. 次のコマンドを使用して、 **/dev/mapper/rootvg-rootlv** のファイル システムのサイズが増加しているかどうかを確認します。

      `#df -Th /`

      出力例:

      ```
      [user@myvm ~]# df -Th /
      Filesystem                Type  Size  Used Avail Use% Mounted on
      /dev/mapper/rootvg-rootlv xfs    12G   71M   12G   1% /
      [user@myvm ~]#
      ```

   > [!NOTE]
   > 同じ手順を使用して他の論理ボリュームのサイズを変更するには、手順 7 で **lv** 名を変更します。

## <a name="next-steps"></a>次のステップ

- [ディスクのサイズ変更](expand-disks.md)