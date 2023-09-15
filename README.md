# adb-dns
enable private dns on android tv


To disable private dns:
```bash
adb shell settings put global private_dns_mode off
```

To enable private dns with hostname:
```bash
adb shell settings put global private_dns_mode hostname
```
Example with dns.nextdns.io:
```bash
adb shell settings put global private_dns_specifier dns.nextdns.io
```
Or with yourID:
```bash
adb shell settings put global private_dns_specifier yourID.dns.nextdns.io
```
Or with yourID, Identify your devices:
```bash
adb shell settings put global private_dns_specifier DeviceName-yourID.dns.nextdns.io
```
Prepend the name to the provided domain (the name should only contain a-z, A-Z, 0-9 and -). Use -- for spaces.
For "anhhp0 AndroidTV", you would use anhhp0--AndroidTV-yourID.dns.nextdns.io.
Example with yourID is 123abc456:
```bash
adb shell settings put global private_dns_specifier anhhp0--AndroidTV-123abc456.dns.nextdns.io
```



