### LibreElec
`mount -o remount, rw /flash` 

`nano /flash/config.txt` 

```
# fan
dtoverlay=gpio-fan,gpio_pin=14,temp=60000
```
```
# ir
dtoverlay=gpio-ir,gpio_pin=3
```
`mount -o remount, ro /flash` 

`reboot` 
