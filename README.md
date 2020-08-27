# hass.media_player.nuvo
Home Assistant - media player - Nuvo multi zone audio amplifier (forked from ejonesnospam/hass.media_player.nuvo)
The nuvo platform allows you to control Nuvo Multi-Zone Amplifier using a serial connection.


- Tested and verified using Home Assistant 0.114.4
- Initially developed/tested with the Nuvo Concerto model NV-I8GM



media_player:
Creates audio media_player units, with sources as defined, for each audio zone defined


To get started download
```
/custom_components/nuvo/manifest.json
/custom_components/nuvo/media_player.py
```
into
```
<config directory>/custom_components/nuvo/
```

**Example configuration.yaml:**

```yawl

  - platform: nuvo
    port: /dev/ttyUSB0
    zones:
      1:
        name: TV
      2:
        name: Basement
      3:
        name: Living Room
      4:
        name: Kitchen
      5:
        name: Bathroom
        
    sources:
      1:
        name: Radio
      2:
        name: Cable

```
### Configuration Variables

**name**

  (string)(Optional) Friendly name of the sensor

**port**

  (string)(Required) Serial or USB connection to RS232 of Nuvo Controller

**zones**

  (string array)(Required) A list of audio zone names
  
**sources**

(string array)(Required) The password for the account


