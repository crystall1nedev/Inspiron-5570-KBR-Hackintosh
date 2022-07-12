# Inspiron-5570-KBR-Hackintosh
Use this if you have the i7-8550U variant of the Inspiron 5570. This EFI works with Monterey 12.0 to Monterey 12.5 beta 3. *For macOS Big Sur support, please see the `big_sur` branch.*

Everything works, credit to phd91105 for the most part with ACPI patches and kexts, just adjusted for this particular model.

**This EFI is not made to be used without modification, and as such issues are disabled.** It is simply here for reference.

Bootloader: Opencore 0.8.2 (release)

Kexts: all updated (as of 07.08.22)

| SPECS |   |
|---|---|
|Motherboard:| Mobile Intel Core i7-8550U, Dell Inspiron 5570|
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
| Intel WiFi | Yes | (Lava: WiFi is noticeably laggier on 5GHz) |
| Intel Bluetooth| Yes | Continuity not completely supported. |
| Realtek Ethernet | Yes | (Lava: Works great, no stability issues.) |
| Touchscreen| Yes | Works like the Magic Trackpad, however taps show as Force Clicks. Disable Force Touch as a workaround. |
| Touchpad | Yes | Works like the Magic Trackpad, clicking shows as Force Clicks. Disable Force Touch as a workaround.|
| Speaker Audio | Yes | (Lava: Works fine, but volume controls change at smaller increments)
| Headphone jack | Yes |
| Power options | Yes | Power Nap should be disabled to prevent the system from turning on and getting stuck. |
| NVRAM | Yes | Emulated |
| iServices | Yes | The serial numbers that are here don't work, you have to make your own. |
| DRM | No | Fairplay does not work properly on the iGPU-only model. Stream with Chrome or download your iTunes movies first. |
| HDMI | Yes | | 
| USB ports | Yes | |
| Fingerprint sensor | No | Fingerprint sensors require T1, T2, or Apple Silicon. |


# Recommended SMBIOS

Use the MacBookPro15,1 SMBIOS for this model. If you experience the "MacBookPro15," problem, make sure that the CustomSMBIOSGUID quirk is enabled and the SMBIOS update method is set to Custom (this EFI in this repo provide this already).
