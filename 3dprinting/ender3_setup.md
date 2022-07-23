# Setup
## Klipper & Mainsail
[Setup](https://theornerymaker.com/?p=321)
[Mainsail](https://all3dp.com/2/mainsailos-simply-explained/)

Raspberry PI Cases
- https://www.thingiverse.com/thing:4192636
- https://www.thingiverse.com/thing:3079477/files

#### Parts Sourcing 
https://www.thingiverse.com/

## OctoPi
[Install Guide](https://all3dp.com/2/ender-3-with-octoprint-how-to-set-up-octoprint-for-your-ender-3/)
[Remote Access](https://octoprint.org/blog/2018/09/03/safe-remote-access/)

Access: 
`http://192.168.1.202/`
`http://octopi.local`

Config: `/etc/wpa_supplicant/wpa_supplicant.conf`
```
## WPA/WPA2 secured
network={
 ssid="<>"
 psk="<>"
}

# Uncomment the country your Pi is in to activate Wifi in RaspberryPi 3 B+ and above
# For full list see: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2
#country=GB # United Kingdom
country=CA # Canada
#country=DE # Germany
#country=FR # France
#country=US # United States
```

OctoPi Plugins: https://all3dp.com/2/must-have-octoprint-plugins/

```
[
{
"key": "themeify", 
"name": "Themeify", 
"url": "https://github.com/birkbjo/OctoPrint-Themeify"
}, 
{
"key": "PrintTimeGenius", 
"name": "PrintTimeGenius Plugin", 
"url": "https://github.com/eyal0/OctoPrint-PrintTimeGenius"
}, 
{"key": "navbartemp", 
"name": "Navbar Temperature Plugin", 
"url": "https://github.com/imrahil/OctoPrint-NavbarTemp"
}, {
"key": "dashboard", 
"name": "Dashboard", 
"url": "https://github.com/j7126/OctoPrint-Dashboard"
}
]
```

## Print Settings
https://all3dp.com/2/ender-3-cura-settings-best-ender-3-cura-profile/

## Upgrades

Bed Knobs - [https://www.thingiverse.com/thing:423...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbWY3V3lzSkxTc0RyV3A0d2lQQXNCYThZVlBsUXxBQ3Jtc0ttdk5FWVM1WHRRM2xyeU5rWUhzQ3NuelpmeWNEelNPOGpsMHVPTUpZc2JwcWI5b2dJd1VNR09TRC16cDVjaXZvR0ZGVXlGNTRNUzJMYXRYSnpjc2ZfQklWLTl5T25oOUh4V0lubmdLZDNGdTFoeFNJdw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A4230695&v=R8CsqU3ijRc) 
LED Light Bar - [https://www.thingiverse.com/thing:327...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa3FWc21HenhQbUdfdVpPX251UlJfaUFMLXk3UXxBQ3Jtc0tuNFoyRHo4b1gxNEUwRnpDMm5URVh0RkRlRW1NMzJ1cEl4WlhxdlFPNkQ5SVRVWUdTbjBmOE1vdFlreDNCN21hN29EWTBiRlhfei1Lc0UyLWt4cFl6RVlCQ2xBWkJxemlqUGV2V0tGcFhlQjNfZ1pUZw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3272248&v=R8CsqU3ijRc) 
Extruder Fan - [https://www.thingiverse.com/thing:334...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbU91dDJRWW1xM056RjJ6Qk1IallaNGt1a0lYd3xBQ3Jtc0ttVDlVODFBNnBHVG9sYkJNbEd3NlJscW9OdkRyM3RrV3RjcWItdE1yVUtybERsa1JYWnpkNGszbUhPa3FmT1pqTnVCNDRmdHF6NnJrMG54RHlvQzFocFFrVE1UYzYwbmhWc2hKbE1UNHM0eTV3ckc1OA&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3343456&v=R8CsqU3ijRc) 
LCD Knob - [https://www.thingiverse.com/thing:482...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbTVqbVlvOXJqbW0zN2JNTEFiZWN5X1NVS2VFQXxBQ3Jtc0tsSVNWSGpGclNVZVpBM2RXaTJSZ2JBb3JOUFdjN3otRkZrLWdzTVJFV2VqdzlUN05lM2V4VkxkZDNHZFZta3ZXUHJsMzV2UlZFUU5neWlYVmQ0YUh4dFhSeWp4SzFSZC1CNnRDb1M2dHdPSmdIUmJ2cw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A4822708&v=R8CsqU3ijRc) 
ail Covers - [https://www.thingiverse.com/thing:337...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbHdXWVRtMDZQYVJlLVZrU2xIRHQ3eGhMVFJ5QXxBQ3Jtc0tuYUM5NEQ3NDNja1pJbG5UcTI0UnU3OEZHVG9GNkU1Zjh0RDh2VXlDVlZ5QjdaYVFjUXlOdHRKc0lEZXZTdXdhVTdTWEt6TlVNc2JpWm1EWFR4dDhFcXZjbG1IbEhMajlBX3pDOXU4N3RZWENXcW5idw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3379068&v=R8CsqU3ijRc) 
Spool Roller (No bearings) - [https://www.thingiverse.com/thing:410...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVZIZlBhYmlDYkZ4ZWg5NERhSUxodUFNRzFkQXxBQ3Jtc0ttc2t6WXZiUkJmSi1hYmJ4OTQ1M0w2VWJyUUpVemlOMXExMFJ6dno2MjdQWFo4QVNva3dRY19UM0s1X2VZQnl0bmZJTzVnYWlYSkpDbjJYdktQQzN0aWIySnM4M0dMeGxLTjFMeHVZMDM2MnByTnlJbw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A4109113&v=R8CsqU3ijRc) 
Spool Roller (With bearings)- [https://www.thingiverse.com/thing:320...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVJPbDJxRTRHTHV2Vk5Wa2JIVEdJdGNmeUhYUXxBQ3Jtc0tsQ2NmOUdRN3R2MTYwRUJlNldaNV9Nd0xkeUk1aXAxbkRvdGpFQWkwNktEejF5bDZZTV9lZnF1bkNBMGZFRFdzUXItMlcwaGwxWDVJU0xfVUkzc1ZnbVlSRXo3bG5Sd2hNNlY5MUR5cDU0TkZ0WDNpdw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3209211&v=R8CsqU3ijRc) 
Filament Guide 1 - [http://www.thingiverse.com/thing:2917932](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmRuUlJKYmFLSXlqcWNidmlSWmMwTm9rYmVoQXxBQ3Jtc0tsV19JbUducHRvdU9aMjZzdExBUmhSMjRDSkhYdTBQeXdqeGRlakhEbGdzZHN3a0tzUnJYMW5SLW9IUlQzdjl0UlFnbW1hWG9qSUxrQ2dyTEJudjVGYWctanA2X3k3T1BITkF3WDZObzlncnVmQ0x1RQ&q=http%3A%2F%2Fwww.thingiverse.com%2Fthing%3A2917932&v=R8CsqU3ijRc) Filament Guide 2 (bearing) - [http://www.thingiverse.com/thing:3052488](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbS1nUjFqLU1Oby00dnJISEs1bV92N2t3emhmQXxBQ3Jtc0trVUtmcklhMUw5N1RwZXp6YXZPOTI1dktEbTRkNkNuWVJoOXppSXRsdmpLZm9sTmNJemgxMmczLXNRZnlPTVBqWkVOSUNRSWpHZTRZb0o5NWY0Sl9FejQwUTBrS3k2eFVBcm9BWFlxOE5HZkxtdmJCSQ&q=http%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3052488&v=R8CsqU3ijRc) 
Bed Handle - [http://www.thingiverse.com/thing:3117709](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbXd5YngzNFRpbUpyZWxvM3JxdFRoWkFMYmpFUXxBQ3Jtc0ttaGZmNXhYeG94cm5ydVBsMnRoaVRmY09DOW9GUm5KOXJvOHhVaUd1WjZNLXR6dElJdE5JOU9BelJuZFFiY0I1NDlDY1FvMTQ0TnhIcUJQM0RyZExBWjB5SEI4WnRlYzE5dGVRYjBVbEFkOE1hVzFQYw&q=http%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3117709&v=R8CsqU3ijRc) 
Fan (by SD card reader) - [https://www.thingiverse.com/thing:293...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa0xCRmliQy1ZdU1zWURlandjNmdZbUxXMUlrd3xBQ3Jtc0trdHJPUWpsY0ZqU01wSXB6NmFDR0pDRjA2ZGRiN0M3RFpESXpiT2xqNm5qZUh4cDZhTTB5NXl4eEJ2M3BQbzF5RFk2MkdrVTRENkVpczZ6OTBVYU5ReDJ3LUZXNHVTZkhfVU5RaDlubWhKMjZLcm9ZNA&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A2935204&v=R8CsqU3ijRc)
Tool Holder - [https://www.thingiverse.com/thing:305...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbktkSFpvTGxONVVVdFhBb2FKTWhJMU93ZGswd3xBQ3Jtc0ttZnd0R0w3WXg4bUN5M09SbFRaZEJOVFB4ckFRbm5sNG4xNXNXNmZJcGVpSEF0N05DOFdGTVZqTnhZNi1aRkhNZTN2V0RmR0EyenRWalZPSUduSHdHam5iOXhLTjR1Y1hySXY5dTlpUWQ3UFNBSVlxVQ&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3057351&v=R8CsqU3ijRc) 
Z Knob - [https://www.thingiverse.com/thing:354...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbHZ0MmpQUE5JQUZ1eDNOM3BteUQ4UGNHeFd4d3xBQ3Jtc0ttM2t1ZXo5NElOT0VOcWRaNnpteGwtTmtYOEdwbFNXU0dPUk82bkNRS0JDRWtUWEdNbFpSYWJYbFI4ZjUwV010SXpfbWQzUjZ0LW01bF9BY1JzZjhsSzFkZ0tHZkNMN3dpWXdmOXBkdEg4eFA2RDhYaw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3548507&v=R8CsqU3ijRc) 
LCD PCP Cover - [http://www.thingiverse.com/thing:2858209](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbTZQYnp0T3RWbUxhNmY1ODcyNlFKdzBEd0U5UXxBQ3Jtc0tsQlphSXB3a1JzRVFqTG8tN20yYngwMV9vakpWTFR0RV9kZ0pOa1lYVlViaVhDR3g2aEtiM1dFbmptQkhjaWZfd1ljRUVaeGVtdmViWk45dkJjSlF2cXNtRzFBcGNsal9mSG9CUEJaVC1QdmtydE02NA&q=http%3A%2F%2Fwww.thingiverse.com%2Fthing%3A2858209&v=R8CsqU3ijRc) Drawer (make sure it is for your correct printer) - [http://www.thingiverse.com/thing:2989218](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbWdMTWlvaFR2NnROTjgzNEt2ZTgtaW03ZTZuUXxBQ3Jtc0tueHFBeHEwb1laNGhaWERrc1JzTC1yUHhjMHBKOHV6V0U1R1FZc0tvSURQVGQxNDZFVGVRcHh6MG9fYk5VVDlPdV9jblJBOEFyWnY5RnlMTTJoaDNxYzB1MnZUb29KTFpRVkdlTWJUdXdaTlpqdld1MA&q=http%3A%2F%2Fwww.thingiverse.com%2Fthing%3A2989218&v=R8CsqU3ijRc) 
Drawer 2 (Ender 3 Pro) - [https://www.thingiverse.com/thing:341...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVNFQWdkRS1RWUs0OTBjOHVITmJCd0tSN0l3UXxBQ3Jtc0tsR1l2ZkwwN0hYMTNobU5HYjZ3VUVRRmp2Z2Y2Ym5aTEN0bFZmcWFVY3Z3dU5pWTdrZjhRQ3drb0dTZFUtLVlxa2VtTWljaFBySEVmRnFNNi1wX1U1eXM5bmNOYzlOQ2NFYU1jODRwMWJmRGd2M194MA&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3416444&v=R8CsqU3ijRc) Chain I used in the video - [https://www.thingiverse.com/thing:376...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmZXaldpaHN3bTc1dnpMSHhHZG1PSXYtVWNJd3xBQ3Jtc0tsbUx3azYzUzhMRUN1WTFDa1hUbE51eXZ2VzlJMDRBYks5b055Qmhvd2xsTHktLS1McXJodS04WlZSMDdWd3JRVTJ1VVBLdm4tWFNCWnVqbFd3ZlI1Q3d2eGhNS3BRanNiZ3FiYXZiRndCUmQ3NWRSWQ&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3769941&v=R8CsqU3ijRc) 
PSU (power supply unit) Fan - [https://www.thingiverse.com/thing:332...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbkdja2VKY1ZQN2p2WVNpRFBPeUoxUGNWM2RMQXxBQ3Jtc0ttcWZoMFR4TDE3ZUFicXhGdHFVR1hUZ0NoN0xCQzlvSFdDbTE3emxzLTRWc0EyYnNONE9HUVlvbGU3WVRNUENSZDRGbDhQNzF1dkZJRjA5OUNGVmFVX0U2YjNJNTRjMzNwcEVTbGZFY1dsSUZyWlpYZw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3328495&v=R8CsqU3ijRc) 
Tool Holder - [https://www.thingiverse.com/thing:387...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa3ctb3ItU0NWZ0lFanQtdUtScVR2Wl96SUlvZ3xBQ3Jtc0tuNnBhMjR0OTF4NnAzb0F6VFhrbUZtbEo5eFZmbUlXSFI2NHg3NS1xVWxLX3pkSFpTVGNHQ0hDMldNZUdwUm4xRXY2MnJ3eGpibS1ldVVrV2ZKajR4SGlqLU0xamF1MGFGN1NfTnFxanQtN0lTZVlQYw&q=https%3A%2F%2Fwww.thingiverse.com%2Fthing%3A3877505&v=R8CsqU3ijRc)

Pi Cam Mount: https://www.thingiverse.com/thing:3586443

