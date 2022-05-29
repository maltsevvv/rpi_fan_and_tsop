![prototype scheme](https://raw.githubusercontent.com/maltsevvv/rpi_fan_and_tsop/master/fan_and_tsop.png)  

# LibreElec
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
