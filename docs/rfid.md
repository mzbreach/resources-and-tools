# RFID Research

The resources here focus on RFID and access-control research from a defensive, educational, and authorized testing perspective. They range from official firmware and hardware pages to community writeups that explain how credential families differ, where common misconceptions come from, and what practical limitations researchers run into.

**Only use these tools and techniques in environments you own or are explicitly authorized to test.**

---

## Core Proxmark3 Resources

- [RfidResearchGroup/proxmark3](https://github.com/rfidresearchgroup/proxmark3) — The main open-source Proxmark3 firmware and client repository maintained by the RFID Research Group. This is the primary reference point for firmware, client commands, hardware support, documentation, and the broader ecosystem around Proxmark3 research.
- [Proxmarkbuilds.org](https://www.proxmarkbuilds.org/) — Download portal for Proxmark3 builds, with notes about firmware differences and installation expectations. Useful when you want prebuilt packages instead of compiling everything yourself.
- [Emulating legacy iClass / iCLASS / Proxmark3 community](https://www.proxmark.io/www.proxmark.org/forum/viewtopic.php%3Fid=6534.html) — Archived Proxmark forum discussion focused on legacy iCLASS behavior and memory layout questions. Helpful as a niche reference when you are trying to understand how older iCLASS credentials store data and where certain assumptions break down.

---

## Hardware and Accessories

- [Proxmark3 RDV4 Kit](https://hackerwarehouse.com/product/proxmark3-rdv4-kit/) — Retail listing for the RDV4 kit from Hacker Warehouse. It is useful mainly as a quick reference for current availability, approximate pricing, and the optional accessory ecosystem around the platform.
- [Proxmark3 RDV4.01](https://www.redteamtools.com/Proxmark3-RDV4.01?searchid=147758&search_query=proxmark) — Another storefront listing for the RDV4.01 hardware. It gives a second source for pricing and product availability and helps show how the device is positioned in red team and hardware research circles.
- [Bluetooth + Battery Module for Proxmark3 RDV4](https://hackerwarehouse.com/product/proxmark3-rdv4-bluetooth-battery-module/) — Add-on module that gives the RDV4 portable, standalone use with onboard battery and Bluetooth connectivity. Useful if you want to understand how researchers make the platform more field-friendly instead of strictly desk-tethered.
- [SAMadams for Flipper Zero](https://www.redteamtools.com/sam-adams-for-flipper-zero/) — Product page for a Flipper Zero add-on built around an HID Secure Access Module. This page is useful less as a shopping link and more as a concise explanation of what a SAM board is, what kinds of credential families it can interact with, and where its limits are.

---

## Community Threads and Troubleshooting Notes

- [Cloning a "NXP MIFARE Classic MFC1C14_x" to a MIFARE Classic 1K?](https://www.reddit.com/r/proxmark3/comments/1h11k1u/cloning_a_nxp_mifare_classic_mfc1c14_x_to_a/) — Reddit thread from a beginner working through MIFARE Classic identification and compatibility questions. Good example of the kinds of practical card-type confusion that come up early when using Proxmark3.
- [Prng detection....... hard (Help with MIFARE Classic 1K - Unable to Retrieve Keys with Proxmark3MAX)](https://www.reddit.com/r/proxmark3/comments/1jcilva/prng_detection_hard_help_with_mifare_classic_1k/) — Troubleshooting thread centered on failed key-recovery attempts against a MIFARE Classic card. Useful as a reminder that field results often depend on card generation, reader behavior, and attack preconditions rather than just running the expected commands.
- [HID iClass Picopass 2K Cloning help](https://forum.dangerousthings.com/t/hid-iclass-picopass-2k-cloning-help/24338) — Community support thread that shows how experienced users help identify whether an iCLASS credential is using standard or elite-style keys and why that distinction matters. Helpful as a real-world troubleshooting example rather than a polished tutorial.
- [HID Iclass proxmark3](https://forum.dangerousthings.com/t/hid-iclass-proxmark3/12674/2) — Short Dangerous Things forum reply that points readers toward a more complete background thread on iCLASS work. Best treated as a navigation breadcrumb into the wider community knowledge base.
- [Need help cloning HID iClass Legacy](https://forum.dangerousthings.com/t/need-help-cloning-hid-iclass-legacy/16334/16) — Forum post documenting one user's experience working through a legacy iCLASS migration problem. Useful as an example of how much care and card-specific validation these workflows require, especially when community posts warn about the risk of damaging tags with incorrect writes.

---

## HID iCLASS Primers and Technical Notes

- [iClass](https://gist.github.com/bettse/36f25f9a2fcca74d773587cc8e780766) — Compact technical primer covering legacy, elite, SR, SE, and SEOS terminology in the HID iCLASS ecosystem. One of the most useful quick-reference pages for understanding credential families, data layout, and why certain attacks work on some cards but not others.
- [HID Secure Identity Object downgrade guide](https://gist.github.com/kitsunehunter/c75294bdbd0533eca298d122c39fb1bd) — A community writeup explaining the concepts behind SIO-based credentials, logical copies, downgrade paths, and reader compatibility caveats. Even if you never follow the workflow itself, it is valuable for understanding the security model and why secure and legacy deployments behave differently.
- [HID iClass proxmark3](https://forum.dangerousthings.com/t/hid-iclass-proxmark3/12674/2) — Useful supporting reference because it points into a broader discussion about practical HID iCLASS research and the tooling commonly used around it.
- [Need help cloning HID iClass Legacy](https://forum.dangerousthings.com/t/need-help-cloning-hid-iclass-legacy/16334/16) — Worth keeping nearby as a cautionary real-world example of the gap between theory and practice when working with legacy iCLASS credentials.

---

## Suggested Reading Order

If you are new to this area, start with the [RfidResearchGroup/proxmark3](https://github.com/rfidresearchgroup/proxmark3) repository to understand the core platform, then read the [iClass](https://gist.github.com/bettse/36f25f9a2fcca74d773587cc8e780766) primer to get familiar with HID credential families. After that, use the Reddit and Dangerous Things threads as troubleshooting references so you can see how terminology, card type, keys, and reader support interact in real-world cases.
