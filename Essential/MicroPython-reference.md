# LEGO SPIKE Essential MicroPython

## Module: hub

### hub.battery object

### hub.bluetooth object

### hub.button.center object

#### hub.button.center.callback()

Returns a function.

#### hub.button.center.is_pressed()

Returns `False` if the button is not pressed, `True` if it is.

#### hub.button.center.on_change()

Returns a function

#### hub.button.center.presses()

Returns the number of times the button was pressed since last call.

#### hub.button.center.was_pressed()

Returns `False` if the button was not pressed since last call,
`True` if it was.

### hub.info()

Returns hub information as dictionary.

Example:
```
{'device_uuid': '03970000-3400-1B00-0A51-333139383836', 'product_variant': 0, 'usb_pid': 13, 'usb_vid': 1684, 'hardware_version': 'Version_D'}
```

### hub.led(*n*)

Changes the color of the power LED. Accepted range 0..10

| value | color |
|-|-|
| 0 | black |
| 1 | magenta |
| 2 | violet |
| 3 | blue |
| 4 | turquoise |
| 5 | mint |
| 6 | green |
| 7 | yellow |
| 8 | orange |
| 9 | red |
| 10 | white |

### hub.motion object

#### hub.motion.gyroscope()

#### hub.motion.accelerometer()

#### hub.motion.yaw_pitch_roll()

#### hub.motion.orientation()

#### hub.motion.gesture()

#### hub.motion constants

| name | value |
|-|-|
| TAPPED | 0 |
| DOUBLETAPPED | 1 |
| SHAKE | 2 |
| FREEFALL | 3 |

### hub.port.A and hub.port.B objects

#### hub.port.A.callback()

Returns a function.

#### hub.port.A.device object

See [Device object](#device-object).

#### hub.port.A.info()

Returns information about the plugged in device as a dictionary.

Example (empty port):
```
{'type': None}
```

#### hub.port.A.mode(n)

#### hub.port.A.pwm(n)

#### hub.port.A.motor object

See the [Motor](#motor) peripherial.

### hub.power_off()

Turns off the hub.

### hub.reset()

Resets the hub.

### hub.status()

Returns hub status as a dictionary.

Example (hub at rest upside down, with two small motors attached to it):
```
{'gyroscope': (0, 0, 0), 'accelerometer': (-24, 6, -1034), 'yaw_pitch_roll': (-84, 0, 178), 'position': (-84, 0, 178), 'port': {'A': [0, 3962, 2, 0], 'B': [0, 6118, -4, 0]}}
```

### hub.temperature()

Returns temperature in Celsius.

### hub constants

| name | value |
|-|-|
| `TOP` | 0 |
| `FRONT` | 1 |
| `RIGHT` | 2 |
| `BOTTOM` | 3 |
| `BACK` | 4 |
| `LEFT` | 5 |

## Module: os

## Module: time

# Peripherials

## Device object

## 3x3 LED Matrix

Cell byte = 16 * *brightness* + *color_index*

The value of *brightness* ranges from 0 to 10. For color indices, 
see [hub.led](#hubledn).

For color indices, 

Example:

```
>>> matrix = hub.port.A.device
>>> matrix.mode(2, b"\xAA\x77\x66\x00\x99\x00\x66\x77\x66")
>>> matrix.get()
[102, 119, 102, 0, -103, 0, -86, 119, 0]
```

## Color Sensor

A call to `hub.port.A.device.get()` returns a 5-element array:

[ *brightness*, *color_index*, *red*, *green*, *blue* ]

## Motor
