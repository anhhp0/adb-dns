# adb-dns
enable private dns on android tv


rem to disable private dns
adb shell settings put global private_dns_mode off

rem to enable private dns with hostname (example with dns.nextdns.io)
adb shell settings put global private_dns_mode hostname
adb shell settings put global private_dns_specifier dns.nextdns.io
rem or with yourID
adb shell settings put global private_dns_specifier yourID.dns.nextdns.io
rem or with yourID, Identify your devices
adb shell settings put global private_dns_specifier DeviceName-yourID.dns.nextdns.io
rem Prepend the name to the provided domain (the name should only contain a-z, A-Z, 0-9 and -). Use -- for spaces.
rem For "anhhp0 AndroidTV", you would use anhhp0--AndroidTV-yourID.dns.nextdns.io

rem to enable private dns with hostname (example with dns.adguard.com)
adb shell settings put global private_dns_mode hostname
adb shell settings put global private_dns_specifier dns.adguard.com
