sudo pvcreate /dev/sdaX

sudo vgcreate vg0 /dev/sdaX

sudo lvcreate -L [SIZE]G -n root vg0

sudo lvcreate -l 100%FREE -n  swap vg0

sudo mkfs.ext4 /dev/vg0/root

sudo mkswap -f /dev/vg0/swap
