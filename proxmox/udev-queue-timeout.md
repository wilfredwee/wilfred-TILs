# Timed out for waiting for udev queue being empty
I spent way too long trying to fix this after a BIOS update.

Mostly referred to this: https://forum.proxmox.com/threads/timed-out-for-waiting-for-udev-queue-being-empty.129481/

1. Get into a shell for the Proxmox host somehow, a few ways:
   - via the WebUI
   - via SSH
   - Mounting it via debug mode
1. in `etc/lvm/lvm.conf`: add `thin_check_options = [ "-q", "--skip-mappings" ]`
1. `update-initramfs -u` (you'll need to be in an actual installed environment, somehow)
