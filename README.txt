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
		- bash.
	* Your linux kernel must have overlayfs and squashfs (if xz compression is not found mksquashfs uses default setting - mostly gzip) module.
	* You should be chrooted to linux distro.
	* You should not be run that tool on *YOUR* **REAL** running linux.

Authors:
	- Daniel K. (https://github.com/danielkot)
Credits:
	- Tomas M. (https://github.com/Tomas-M)
