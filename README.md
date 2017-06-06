# Lenovo 300 17ISK 15ISK 14ISK 10.12 Clover

Contains Clover 4077 EFI folder with all SSDT patches and required kexts. Testetd on model Lenovo 300-17ISK 80QH without discrete grapics. Used only integrated HD520 graphics. This EFI tested on Mac OS Sierra 10.12.5.

# Installation

Make bootable MacOS Sierra 10.12.x image first. Second place the EFI folder in root of USB drive that you want to use for installer. When system boot from installer set ig-platform-id value to "test" and boot installer. After installing a system system will have to boot normaly but if you get kernel panic on SKL framebuffer just set ig-platform-id to "test" again and boot system normal. Then rebulid a cache using `sudo kextcache -i /` and you graphics will work perfect after reboot.

# Where to get installer for 10.12.x

Create bootable USB using create media install command from AppStore or just download BDU image with system installer.
