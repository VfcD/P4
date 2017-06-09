# P4

### Backup anlegen:
  
     mount /dev/sdX2 /mnt
     mount /dev/sdX1 /mnt/boot

### BackupVerzeichnis erstellen!
  
    mkdir ~/ArchBackup
    rsync -avz /mnt/ ~/ArchBackup/

    umount /mnt/boot
    umount /mnt

### SD-Karte Wechseln!


### https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-3

Schritt 1 und 2 ausführen

Schritt 3

    mkfs.vfat /dev/sdX1
    mkfs.ext4 /dev/sdX2

Schritt 4

    mount /dev/sdX2 /mnt
    mkdir /mnt/boot
    mount /dev/sdX1 /mnt/boot
    rsync -avz ~/ArchBackup/ /mnt
    umount /mnt/boot
    umount /mnt
    
    
 # Fertig!
