This guide works well:
https://clearlinux.org/documentation/clear-linux/get-started/virtual-machine-install/kvm

But you need to add your user to the kvm & qemu groups
```
$ usermod -aG kvm,qemu $USER
```

Resizing an image can be done via:
```
$ qemu-img resize ./clear.img +20G
```
Then follow this guide to expand the partition https://clearlinux.org/documentation/clear-linux/guides/maintenance/increase-virtual-disk-size.

Note: DO NOT use the fdisk method of expanding the partition, it renders the image unbootable.
