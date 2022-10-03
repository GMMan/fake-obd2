Super OBD2 (2019-01)
====================

|                    |                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------|
| Name               | Super OBD2                                                                                  |
| Purchase date      | 2019-01                                                                                     |
| Color              | Yellow                                                                                      |
|Purchase link|[eBay](https://www.ebay.ca/itm/273571561327), seller [clother_trade](https://www.ebay.ca/usr/clother_trade)|
| Type               | MCU-based non-connected                                                                     |
| Power draw | 5-10mA |
| MCU                | Unknown 14-pin                                                                              |
| Pins through board | 4 (GND), 5 (GND), 6 (CAN high), 7 (K-Line), 8 (disc.), 14 (CAN low), 15 (L-Line), 16 (+12V) |
| Pins routed        | 4 (GND), 5 (GND), 16 (+12V)                                                                 |
| Board layers       | 2                                                                                           |

This one doesn't connect to anything, but has a somewhat more convincing LED
flash pattern, which begins with some quick blinking of the OBD LED to pretend
it's installing something, then after that slow blink the same LED a few times
and waits some amount of time before blinking some more, cycling through three
different delays. Interestingly, the static LEDs are PWM-driven at about 100Hz.

All the pins not connected to something else appear to be pulled low
internally, with no activity on them. Did not really test trying to apply a
signal to those pins.

LED pattern
-----------

| Time (s) | Red 1     | Red 2           | Green |
|----------|-----------|-----------------|-------|
| 0        | Off       | Off             | Off   |
| 1        | Solid     | Solid           | Solid |
| 4        | Off       | Off             | Solid |
| 5        | Solid     | Slow flashing   | Solid |
| 7        | Solid     | Off             | Solid |
| 9        | Solid     | Fast flashing   | Solid |
| 69       | Solid     | Medium flashing | Solid |
| 70       | Solid     | Off             | Solid |
| 120      | Solid     | Medium flashing | Solid |
| 121      | Solid     | Off             | Solid |
| 154      | Solid     | Medium flashing | Solid |
| 155      | Solid     | Off             | Solid |
| 170      | Go to 69s |                 |       |

Photos
------

### Packaging

<table>
<tbody>
<tr>
<td><a href="packaging/package_front.jpg"><img src="thumbs/package_front_t.jpg" alt="Package front"></a></td>
<td><a href="packaging/package_back.jpg"><img src="thumbs/package_back_t.jpg" alt="Package back"></a></td>
</tr>
<tr>
<td><a href="packaging/package_side.jpg"><img src="thumbs/package_side_t.jpg" alt="Package side"></a></td>
<td><a href="packaging/package_inside.jpg"><img src="thumbs/package_inside_t.jpg" alt="Package inside"></a></td>
</tr>
</tbody>
</table>

Other sides of the box had nothing printed.

### Device shell

<table>
<tbody>
<tr>
<td><a href="shell/front.jpg"><img src="thumbs/front_t.jpg" alt="Shell front"></a></td>
<td><a href="shell/back.jpg"><img src="thumbs/back_t.jpg" alt="Shell back"></a></td>
</tr>
<tr>
<td><a href="shell/top.jpg"><img src="thumbs/top_t.jpg" alt="Shell top"></a></td>
<td><a href="shell/bottom.jpg"><img src="thumbs/bottom_t.jpg" alt="Shell bottom"></a></td>
</tr>
<tr>
<td><a href="shell/left.jpg"><img src="thumbs/left_t.jpg" alt="Shell left"></a></td>
<td><a href="shell/right.jpg"><img src="thumbs/right_t.jpg" alt="Shell right"></a></td>
</tr>
</tbody>
</table>

### Board

<a href="board/board.jpg"><img src="thumbs/board_t.jpg" alt="Board"></a>

Bottom of the board only has a few traces, no components.

Schematic
---------

![Schematic](board/schematic.png)

No debouncing capacitor on reset button, and no decoupling capacitors fitted
anywhere, very weird. There's a second reset button position so the same board
can be used on the ecoOBD2 type shell.
