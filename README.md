# VirtualBox
A VirtualBox VM Image that runs Python KMS as a systemd service.

## Download The Image
First you'll need to download the image and import it into VirtualBox.

MEGA - https://mega.nz/file/NWUDEBxR#WpvjUPhoKI3xBsn7JQPM_tN82MUkDCxIfh2k3eXGD00

## Get the IP Address
Login to the VM with the username `ubuntu` and the password `password`. Type `ip addr` to get the VM's IP Address.

## Activate Windows
Open a CMD prompt as administator. Type `cscript slmgr.vbs /skms ip` then open Windows setting, visit the activation screen and change your product key and enter your GVLK key from https://py-kms.readthedocs.io/en/latest/Keys.html. From there run `cscript slmgr.vbs /ato`. Once you get a popup saying the activation was complete you can shutdown the VM and restart your computer.

## Reactivations
Windows needs to check in with the KMS server at least once every 180 days or Windows will become unactivated. The VM has a very light footprint so you can keep it running most of the time with no impact. Although as long as you start it, run the `cscript slmgr.vbs /ato` command, you can turn it back off for another 180 days.
