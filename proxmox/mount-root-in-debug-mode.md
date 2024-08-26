# Mounting the Proxmox root filesystem if you can't boot into it.
- If you absolutely can't boot into your Proxmox system, i.e. you can't get a shell in your Proxmox environment, one thing you can do is to use the Proxmox ISO Debug Mode to get into a shell, then mount your _installed_ Proxmox.

1. Boot into Proxmox live ISO.
1. Select Advanced Options -> Install PVE (Debug Mode)
1. Type 'exit' to exit into a shell.
1. Mount the _installed_ Proxmox (roughly obtained from [here](https://superuser.com/questions/116617/how-to-mount-an-lvm-volume)):
   1. `vgscan` to get the pve-root group.
   1. `vgchange -ay pve`. sub `pve` with whatever you got from `vgscan`. This will 'activate' the volume.
   1. `lvs` to get the pve-root volume, this is likely `root`
   1. `mkdir /mnt/whatever`
   1. `mount /dev/pve/root /mnt/whatever`
1. You'll likely need to mount `/sys`, `/dev` and others too, but I lost the link/code to these so you'll have to figure it out.
1. Then `chroot /mnt/whatever`. Now you are effectively working in the _installed_ Promox environment.
1. You can for example change the `/etc/lvm/lvm.conf` file. (Though you don't really need `chroot` for this, just mount it)
1. I didn't figure out how to get networking setup so that I can do `apt update` though.
