# LEGO Education SPIKE Esssential HUB

Also known as **LEGO Technic Small Hub**.

Upon connecting either through USB or through Bluetooth, the hub presents 
a serial device (on Linux, `/dev/ttyACM0` and `/dev/rfcomm0`, respecitvely) 
and attempts writing to it. If it does not succeed for 10 seconds, it shuts down.

If connected to a serial terminal emulator (e.g. `picocom`), its startup process 
(`hub_runtime.start()`) will flood the screen with sensor readings, but it can be 
stopped by **Ctrl + C** and one gets a MicroPython console prompt.
