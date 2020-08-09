# This repository is no longer maintained original repo https://github.com/Gr4ffy/lede-cups.git

# How to install Cups on OpenWrt/LEDE
https://github.com/TheMMcOfficial/cups-for-openwrt

# How to compile the Packages
```
git clone https://github.com/lede-project/source

cd source

echo "src-git cups https://github.com/TheMMcOfficial/lede-cups.git" >> feeds.conf.default

./scripts/feeds update -a

./scripts/feeds install -a

make menuconfig (set Network->Printing->cups as "M")

make

copy /source/bin/packages/[PLATFORM]/cups/*.ipk to machine & opkg install 
```
# Version of cups

In any case:
## If you just want to attach your printer and use it from another PC using CUPS is most likely a bad idea

## Included packages
* libcups
  * The cups core libraries required to run cups or any drivers
* libcupsimage
  * Library to allow CUPS to work with rasterized data
* cups
  * The common unix printing system (cups) daemon itself
* cups-bsd
  * Some BSD-type utilities (lprm,lpq,lpr,lpc)
* cups-client
  * Advanced client utilities (lp,cancel,cupstestppd,ipptool,lpoptions,lpstat,cupsaccept,cupsfilter,lpadmin,lpinfo,lpmove)
* cups-filters-lite
  * Some basic printer filters (commandtops,gziptoany,pstops,rastertoepson,rastertohp,rastertolabel,rastertopwg)
* cups-ppdc
  Compiler for PPDC files (deprecated)
* cups-bjnp
  * Filter for Canon printers using canon printers using USB over IP BJNP
* cups-dymo
  * Official drivers for Dymo label printers
* cups-opfilter
  * Filters to convert JPEG, PNG or TIFF images to raster data suitable for some printers

## Sources/Credits
* Original: https://github.com/Gr4ffy/lede-cups
* Via: https://github.com/lllrrr/lede-cups

## Version of cups
2.3.0
