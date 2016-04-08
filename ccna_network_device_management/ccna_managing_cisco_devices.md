# Managing Cisco Devices

## Changing the Configuration Register
Inside IOS
```
show version

conf t
config-register 0x2101
exit
copy runnign-config startup-config

show version
```

Outside IOS
```
confreg 0x2142
```

## Password Recovery
1. Switch off the router
2. Switch on the router. Press **Break** to enter ROM monitor mode
3. When the router is in ROM monitor mode, set the configuration register to 0x2142
```confreg 0x2142```
4. Reset the router
```reset```
5. Enter privileged EXEC mode
```enable```
