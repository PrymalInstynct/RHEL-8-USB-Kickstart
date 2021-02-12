# RHEL-8-USB-Kickstart
Examples of RHEL 8 Kickstart files that work on USB Media

## ks-usb.cfg
RHEL 8 install Anaconda Config that utilizes a USB Storage Device for the boot media and targets a traditional BIOS Install

## ks-disc.cfg
RHEL 8 install Anaconda Config that utilizes the Physical/Virtual Disc Drive for the boot media and targets a UEFI BIOS Install

## Creating the Kickstart Enabled ISO
Dependencies
------------
- RHEL 8 Machine registered with Subscription Manager
- CentOS 8 Machine
- Anaconda Kickstart File configured and Copied to Build machine

```
dnf -y install lorax yum-utils python3
wget -cN https://raw.githubusercontent.com/weldr/lorax/master/src/sbin/mkksiso
chmod +x mkksiso
./mkksiso ks-usb.cfg rhel-8.3-x86_64-dvd.iso rhel-8.3-x86_64-kickstart-usb.iso
```
