# P4

### Backup anlegen:
  
     mount /dev/sdx2 /mnt
     mount /dev/sdx1 /mnt/boot

### BackupVerzeichnis erstellen!
  
    mkdir ~/ArchBackup
    rsync -avz /mnt/ ~/ArchBackup/

    umount /mnt/boot
    umount /mnt


https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-3

Schritt 1 und 2 ausführen

Schritt 3

    mkfs.vfat /dev/sdx1
    mkfs.ext4 /dev/sdx2

Schritt 4

    mount /dev/sdx2 /mnt
    mkdir /mnt/boot
    mount /dev/sdx1 /mnt/boot
    rsync -avz ~/ArchBackup/ /mnt
    umount /mnt/boot
    umount /mnt
