### LibreElec
`mount -o remount, rw /flash` 

`nano /flash/config.txt` 

```
# fan enable if temp 65C
dtoverlay=gpio-fan,gpio_pin=14,temp=65000
```
```
# ir
dtoverlay=gpio-ir,gpio_pin=3
```
`mount -o remount, ro /flash` 

`reboot` 
