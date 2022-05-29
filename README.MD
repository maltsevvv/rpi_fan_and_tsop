![prototype scheme](https://raw.githubusercontent.com/maltsevvv/rpi_fan_and_tsop/master/fan_and_tsop.png) 

# LibreElec
`mount -o remount, rw /flash` 

`nano /flash/config.txt` 

```
# fan enable if temp 65C
dtoverlay=gpio-fan,gpiopin=14,temp=65000
```
```
# ir
dtoverlay=gpio-ir,gpio_pin=3
```
`mount -o remount, ro /flash` 

`reboot` 

# Raspbian
`sudo nano /boot/config.txt` 

```
# fan enable if temp 65C
dtoverlay=gpio-fan,gpio_pin=14,temp=65000
```
```
# ir
dtoverlay=gpio-ir,gpio_pin=3
```
`reboot` 


## LibreElec
`systemctl stop kodi` 

`systemctl stop eventlircd` 

#### Смотрим допустимые протоколы 
`ir-keytable`

#### Смотрим коды кнопок с протоколом nec 
`ir-keytable -p nec -t`

#### Создаем коды и идентификаторы для kodi 

`nano /storage/.config/rc_keymaps/samsung` 
```
# table samsung, type: nec

0x70702 KEY_POWER
0x70760 KEY_UP
0x70761 KEY_DOWN
0x70765 KEY_LEFT
0x70762 KEY_RIGHT
0x70768 KEY_OK
0x70758 KEY_BACK
0x70747 KEY_PLAY
0x7074a KEY_PAUSE
0x70746 KEY_STOP
0x7072b KEY_HOME
```

#### Создать файл
`nano /storage/.config/rc_maps.cfg`
```
* * samsung
```

