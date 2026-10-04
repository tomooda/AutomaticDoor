# Automatic Door

This is an example specification of an autmatic door in VDM-SL.
The door is closed when standing by, and should automatically open to allow people passing through.
The system consists of 3 modules: the `Sensor` module that detects human bodies nearby, the `Motor` module that moves the door, and the `AutomaticDoor` module that controls the entire system.

## The `Sensor` module

The `Sensor` module is a stub of real sensors.

### states

To mimic the functionality of the real sensor, this module has one state variable `sensor`.
```vienna-source|module=Sensor
Sensor
```

### operations

The `detect` operation is the main feature of this module to detect a human nearby.
```vienna-source|module=Sensor
detect
```

The `setSensor` operation swtches the state of sensor whether a human body is detected or not.
```vienna-source|module=Sensor
setSensor
```

### sandbox

```vienna-exec|module=Sensor&state=no
detect()
```
```vienna-exec|module=Sensor&state=diff
setSensor(true)
```
```vienna-exec|module=Sensor&state=diff
setSensor(false)
```
```vienna-watch|module=Sensor
sensor
```
### source

```vienna-source|module=Sensor
```

