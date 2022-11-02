PowerProg (2022-09)
===================

|                    |                                                                                                                                                                                                   |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name               | PowerProg (Diesel)                                                                                                                                                                                |
| Purchase date      | 2022-09                                                                                                                                                                                           |
| Color              | Red                                                                                                                                                                                               |
| Purchase link      | [eBay](https://www.ebay.com/itm/175293384684?var=474511759085), seller [value1992](https://www.ebay.com/str/value1992)                                                                            |
| Type               | Analog flasher, non-connected                                                                                                                                                                     |
| Power draw         | Unmeasured (power source not 12V)                                                                                                                                                                 |
| MCU                | N/A                                                                                                                                                                                               |
| Pins through board | 1* (disc.), 2* (J1850+), 3* (disc.), 4 (GND), 5 (GND), 6 (CAN high), 7 (K-Line), 8 (disc.), 9* (disc.), 10* (J1850-), 11* (disc.), 12* (disc.), 13* (disc.), 14 (CAN low), 15 (L-Line), 16 (+12V) |
| Pins routed        | 4 (GND), 5 (GND), 16 (+12V)                                                                                                                                                                       |
| Board layers       | 2                                                                                                                                                                                                 |

\* Pins have holes in board but are snipped off on housing

This one is using a simple astable multivibrator to blink one LED while leaving
two other LEDs always lit. Compared to [ecoOBD2 (diesel)](../eco_obd2_diesel_2022-09/README.md),
the button turns off the entire board while pressed instead of just resetting
the flashing LED. No connection to busses.


LED pattern
-----------

Solid red and green, amber blink on for ~0.25s, off for ~0.75s.

Photos
------

<table>
<tbody>
<tr>
<td><a href="packaging/box_front.jpg"><img src="thumbs/box_front_t.jpg" alt="Box front"></a></td>
<td><a href="packaging/box_back.jpg"><img src="thumbs/box_back_t.jpg" alt="Box back"></a></td>
</tr>
<tr>
<td><a href="packaging/box_left.jpg"><img src="thumbs/box_left_t.jpg" alt="Box left"></a></td>
<td><a href="packaging/box_right.jpg"><img src="thumbs/box_right_t.jpg" alt="Box right"></a></td>
</tr>
<tr>
<td><a href="packaging/box_top.jpg"><img src="thumbs/box_top_t.jpg" alt="Box top"></a></td>
<td><a href="packaging/box_bottom.jpg"><img src="thumbs/box_bottom_t.jpg" alt="Box bottom"></a></td>
</tr>
</tbody>
</table>

It says Super OBD2 for some reason instead of PowerProg.

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

The only printing on it is on the front. Shell was kind of difficult to unclip.

### Board

<a href="board/board.jpg"><img src="thumbs/board_t.jpg" alt="Board"></a>

It kind of looks like they chopped the top of the button off.

Schematic
---------

![Schematic](board/schematic.png)

Just an astable multivibrator made of discrete components, but with whole
board power off. Interesting to note that it's still a YM-701 of sorts, even
though the other versions use a dual op amp. Perhaps not enough space for that
here.
