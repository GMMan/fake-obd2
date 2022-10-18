The Fake OBD-II Tuning Box Collection
=====================================

This repo contains photos and info on my collection of fake OBD-II tuning
boxes.

What are these things?
----------------------
OBD-II chip tuning boxes purportedly adjusts your car engine's operating
parameters by communicating to the ECU through your car's OBD-II port, to
either increase the engine's power, or to reduce fuel usage. However, these
low-cost devices generally don't actually communicate with your ECU. They
typically just flash some LED. Sometimes they may be connected to your car's
CAN bus lines, but have high value resistors that result in them only being
able to listen to traffic rather than send any. At best these are a waste of
battery if you leave them plugged in while the vehicle is off, and at worst
may potentially cause issues with your car's internal network if the device
is miswired. As such, plese don't buy these devices if you expect them to help
with your car's performance. They will only serve as a light show.

[Big Clive](https://www.youtube.com/channel/UCtM5z2gkrGRuWd0JQMx76qA) has some
video teardowns of these devices, by type:
- [MCU-based CAN bus monitoring](https://www.youtube.com/watch?v=zx8fywphQp0)
- [MCU-based CAN bus direct connect](https://www.youtube.com/watch?v=PB810U7j77k)
- [MCU-based non-connected](https://www.youtube.com/watch?v=azuB9ZJuDlM)
- [Analog flasher, non-connected](https://www.youtube.com/watch?v=axow7KnBtaM)

What are the types?
-------------------

### MCU-based monitoring

These types use a microcontroller and monitors CAN bus, ISO 9141, and/or SAE
J1850 bus through a high-value resistor. These may or may not use the traffic
on those buses to flash the LEDs differently.

### MCU-based direct connect

These types use a microcontroller and are directly connected to the above
buses. They may be able to drive the buses or otherwise wreak havoc if the
microcontroller crashes.

### MCU-based non-connected

These types use a microcontroller and are not connected to the buses at all.
They are not influenced by or can influence the buses in any way, and are
purely for show.

### Analog flasher

These don't use a microcontroller and just flash a LED using analog circuitry.

What have you got?
------------------

Click the photo/name of the device for details, photos, and schematic.

| Photo | Name       | Purchase date | Color  | Type                               |
|-------|------------|---------------|--------|------------------------------------|
|[![ecoOBD2](eco_obd2_2019-01/thumbs/front_t.jpg)](eco_obd2_2019-01/README.md)       | [ecoOBD2](eco_obd2_2019-01/README.md)    | 2019-01       | Green  | MCU-based non-connected/monitoring |
|[![Super OBD2](super_obd2_2019-01/thumbs/front_t.jpg)](super_obd2_2019-01/README.md)       | [Super OBD2](super_obd2_2019-01/README.md) | 2019-01       | Yellow | MCU-based non-connected            |
|[![nitroOBD2](nitro_obd2_2022-09/thumbs/front_t.jpg)](nitro_obd2_2022-09/README.md)       | [nitroOBD2](nitro_obd2_2022-09/README.md) | 2022-09       | Yellow | Analog flasher, non-connected            |
