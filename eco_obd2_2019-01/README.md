ecoOBD2 (2019-01)
=================

|                    |                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------|
| Name               | ecoOBD2                                                                                     |
| Purchase date      | 2019-01                                                                                     |
| Color              | Green                                                                                       |
|Purchase link|[eBay](https://www.ebay.ca/itm/153220768827), seller [loristar](https://www.ebay.ca/usr/loristar)|
| Type               | MCU-based non-connected/monitoring*                                                         |
| Power draw | 6-10mA |
| MCU                | Unknown 8-pin                                                                               |
| Pins through board | 4 (GND), 5 (GND), 6 (CAN high), 7 (K-Line), 8 (disc.), 14 (CAN low), 15 (L-Line), 16 (+12V) |
| Pins routed        | 4 (GND), 5 (GND), 6* (CAN high), 7* (K-Line), 14* (CAN low), 15* (L-Line), 16 (+12V)        |
| Board layers       | 1                                                                                           |

\* Routed, but components not fitted to make a connection to the MCU

This one looked like it's capable of receiving signals from a couple of the
vehicle's networks to dynamically flash its LEDs in response, but the
components connecting those lines to the MCU are not fitted. The MCU
didn't do anything interesting when the two unconnected pins were pulled up
and down. In fact it seemed to loop the same short flashing sequence over
and over. Fairly uncreative.

LED pattern
-----------

| Time (s) | Red    | Amber        | Green |
|----------|--------|--------------|-------|
| 0        | Solid  | Solid        | Solid |
| 5        | Off    | Off          | Solid |
| 6        | Solid  | Slow flash   | Solid |
| 8        | Solid  | Off          | Solid |
| 10       | Solid  | Fast flash   | Solid |
| 20       | Solid  | Medium flash | Solid |
| 21       | Solid  | Off          | Solid |
| 30       | Off    | Off          | Off   |
| 32       | Repeat |              |       |

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
<td><a href="packaging/insert_front.jpg"><img src="thumbs/insert_front_t.jpg" alt="Insert front"></a></td>
<td><a href="packaging/insert_back.jpg"><img src="thumbs/insert_back_t.jpg" alt="Insert back"></a></td>
</tr>
<tr>
<td><a href="packaging/insert_inside_top.jpg"><img src="thumbs/insert_inside_top_t.jpg" alt="Insert inside top"></a></td>
<td><a href="packaging/insert_inside_bottom.jpg"><img src="thumbs/insert_inside_bottom_t.jpg" alt="Insert inside bottom"></a></td>
</tr>
</tbody>
</table>

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

Schematic
---------

![Schematic](board/schematic.png)

Note the diodes on the bus lines. If fitted, they are designed to prevent
any output from the microcontroller from reaching the vehicle's network.
