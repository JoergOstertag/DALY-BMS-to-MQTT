Examples for IOT integrations
-----------------------------

In this directory you can find example configurations for openhab and homeassist.
They add a basic support for the mqtt messages sent by a DALY-BMS-to-MQTT device.

In the examples the mqtt topic is starting with DALY-0/, please adapt if you have configured a different name and start topic in your device.


Directories:
------------


openhab:
--------

This contains the example configurations for openhab. A prerequesite is a completely configured mqtt support.

These two files go into the openhab directory /etc/openhab/
 - things/mqtt-daly.things
 - items/mqtt-daly.items

After inserting these files you can use the resulting Items in your own integration.


homeassist:
-----------

This contains the example configurations for homeassist. 
A prerequisite is a completely configured mqtt support.

To insert into your setup you can add something like the following into your configuration.yaml:

```yaml
 homeassistant:
   packages: !include_dir_named packages
```

This will add all (corectly spelled) yaml files into the main HomeAssist configuration.
