# WVC-Inverter-R2-R3-HC-12--and--Modem

bash serial interfcace  using interceptty as  serial sniffer . It works with  both the original WVC r2 modem  for r2 inverters ( 2 byte inverters IDs).
It also works with HC-12 module -  this will work with all versions of WVC inverter 2 byte inverter  IDs (R2) and 4 byte inverter IDs (R3).
prerequisite additional software: interceptty ( serial sniffer), jq ( Json query software)

 interceptty  --  https://github.com/geoffmeyers/interceptty
 
jq - found in your  distro software  libary 

if installing on openwrt router you will also need to install

for openwrt Compatiblity _
install bash grep stty bc tac  the openwrt binary for interceptty are found in the interceptty folder plus you need  to modify line  ps -efww  in wvc and remove the ps arguements -efww


the command line for HC-12 module-
 
wvc /dev/ttyUSB0 /home/user/WVC/wvc.ini fb041185 hc

command line for WVC modem -  fb041185 being your modem ID

wvc /dev/ttyUSB0 /home/stephen/WCVF/wvc.ini fb041185 modem

modify wvc.ini to match your inverter IDs 

supported inverters are WVC295, WVC300, WVC350, WVC600,WVC700 WVC850, WVC1200 and WVC1400

R2 and R3 denote the inverter  versions 

WVC1200/c784/R2
WVC700/ 4000c784/R3

