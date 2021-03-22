# Inspiron-5570-KBR-Hackintosh
Use this if you have the i7-8550U variant of the Inspiron 5570 (no descrete GPU). 

Everything works, credit to phd91105 for the most part with ACPI patches and kexts, just adjusted for this particular model.

Bootloader: Opencore 0.6.7

Kexts : all updated

| SPECS |   |
|---|---|
|Motherboard:| Mobile Intel Core i5-8550U, Dell Inspiron 5570|
|System Memory| 12288 MB (DDR4 RAM)|
|Display:| Intel UHD Graphics 620|
|Monitor|Dell RN91N [15.6" LCD]|
|Audio Adapter| Realtek ALC256 @ Intel Sunrise Point-LP PCH - High Definition Audio Controller [F0]|
|Storage:| LITEON CV8-8E128-11 128GB (PCIe)|
|Network:| Intel Wireless-AC 3125|

# What works?

| Function | Works? | Extra comments |
|-----------|--------| ---------------|
| GPU acceleration | Yes | Even though the framebuffer is not recommended, this one performs better. |
| Intel WiFi | Yes | | 
| Intel Bluetooth| Yes | May have problems with any headset connected. A fix is to disable WiFi. |
| Realtek Ethernet | Yes | |
| Touchscreen| Yes | Works like the Magic Trackpad, however taps show as Force Clicks. |
| Touchpad | Yes | Works like the Magic Trackpad, pressing down and clicking is Force Touch. |
| Speaker Audio | Yes |
| Headphone jack | Yes |
| Power options | Yes | Power Nap should be disabled to prevent the system from turning on and getting stuck. |
| NVRAM | Yes | Emulated |
| iServices | Yes | The serial numbers that are here don't work, you have to make your own. |
| DRM | No | Fairplay does not work properly on the iGPU-only model. Stream with Chrome or download your iTunes movies first. |
| HDMI | Yes | |
| USB ports | Yes | |
| Fingerprint sensor | No | Fingerprint sensors require the T2 chip. |


I'm working on fixing anything that doesn't work properly. Here's my to-do:

* Fix sleeping problems
* Potentially emulate the T2 chip for fingerprint sensors (?)

# Recommended SMBIOS

Use the MacBookPro16,3 SMBIOS for this model. If you experience the "MacBookPro16," problem, make sure that the CustomSMBIOSGUID quirk is enabled and the SMBIOS update method is set to Custom (this EFI in this repo provide this already).

# Note about the EFI

This EFI is provided to work without any problems, all you need to do is change the SMBIOS variables and you'll be all set with a perfectly tolerable Hackintosh. If, for any reason, something doesn't work properly, you should open an issue on this repo and detail what's wrong.
