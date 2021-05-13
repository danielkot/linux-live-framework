Minimal Linux Booter
====================

This project is to minimize Linux-Live Kit (https://github.com/Tomas-M/linux-live)

Note:
	* Your distro must have installed:
		- squashfs-tools,
		- genisoimage or mkisofs,
		- cpio,
		- gzip,
		- sed,
		- grep,
		- rsync,
		- syslinux-utils,
		- bash,
		- (Optionally) mdadm.
	* Your linux kernel must have overlayfs and squashfs module.
		- If xz compression is not found, mksquashfs uses default settings - mostly gzip.
	* Installer is included in this project.
		- In your booted linux distro, open terminal and type as root `install-linux`.
		- In order to install your distro to hdd you also must have installed:
			- dialog,
			- fdisk,
			- cfdisk,
			- mke2fs,
			- grub2.
	* You can also boot your linux distro in frugal mode (for Windows and Linux):
		- For Linux (All hdd free space in frugal mode):
			- Boot your linux distro,
			- Format partition (for ex. /dev/sda1) as linux filesystem (for ex. ext4),
			- Create directory (for ex. /mnt/sda1),
			- Mount /dev/sda1 to /mnt/sda1,
			- Create loop directory to unpack files from iso image (for ex. /mnt/iso),
			- Mount YOUR_BUILT_LINUX_DISTRO_WITH_THIS_TOOL.iso /mnt/iso,
			- Copy files from /mnt/iso to /mnt/sda1,
			- cd to /mnt/sda1,
			- Add executable permission by: `chmod +x bootinst.sh`,
			- Run: `./bootinst.sh`,
			- Cleanup: `umount -f /mnt/sda1 /mnt/iso && rmdir /mnt/sda1 /mnt/iso`,
			- Now `reboot` to your frugal mode linux distro.
		- For Windows (Only 4 GB free space in frugal mode due to fat32 limits):
			- Format partition (for ex. d:\) to fat32 (is more stable that ntfs),
			- Copy files from iso image to formated d:\,
			- Open cmd as admin,
			- cd to d:\,
			- Run in cmd `bootinst.bat`,
			- Now you can reboot your device to your linux distro,
		- OR Use rufus to write image to pendrive.
	* The iso image uses legacy MBR bootloader and UEFI.
		- The `install-linux` uses legacy MBR bootloader at this time!
	* You should be chrooted to linux distro.
	* You should not be run that tool on *YOUR* **REAL** running linux.
	* The final iso image will be in your root device (means /) (If you ran this tool in *YOUR* **REAL** running linux) or in your chrooted linux distro (means /path/to/chroot/folder).

Authors:
	- Daniel K. (https://github.com/danielkot)
Credits:
	- Tomas M. (https://github.com/Tomas-M)
