# CUPS for OpenWRT/LEDE

This is a playground for one of my systems and mostly _UNMAINTAINED_. Check Upstream for a less fscked up version. Still:

## If you just want to attach your printer using this is most likely a bad idea

## Sources/Credits
* Original: https://github.com/Gr4ffy/lede-cups
* Via: https://github.com/lllrrr/lede-cups
* Maintained: https://github.com/TheMMcOfficial/lede-cups (yes, even if it says it's not ;))

## Installation
* git clone https://git.openwrt.org/openwrt/openwrt.git
* cd openwrt
* (if required git checkout ***version***)
* echo "src-git cups https://github.com/adlerweb/lede-cups.git" >> feeds.conf.default
* ./scripts/feeds update -a
* ./scripts/feeds install -a
* make menuconfig (set Network->Printing->cups as "M")
* make
* copy /source/bin/packages/[PLATFORM]/cups/*.ipk to machine & opkg install 

## Version of cups
2.3.0
