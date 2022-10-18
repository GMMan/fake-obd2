nitroOBD2 (2022-09)
===================

|                    |                                                                                                                                                                                                                                                                                                                     |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name               | nitroOBD2 (Benzine)                                                                                                                                                                                                                                                                                                 |
| Purchase date      | 2022-09                                                                                                                                                                                                                                                                                                             |
| Color              | Yellow                                                                                                                                                                                                                                                                                                              |
| Purchase link      | [eBay](https://www.ebay.com/itm/363856147846), seller [solarf5780](https://www.ebay.com/str/solarf5780)<br>[eBay](https://www.ebay.com/itm/313561026568), seller [ffaut_14](https://www.ebay.com/str/ffaut14)<br>[eBay](https://www.ebay.com/itm/313901552520), seller [ffaut_14](https://www.ebay.com/str/ffaut14) |
| Type               | Analog flasher, non-connected                                                                                                                                                                                                                                                                                        |
| Power draw         | 7mA                                                                                                                                                                                                                                                                                                                 |
| MCU                | Unknown 8-pin, pinout like Toshiba                                                                                                                                                                                                                                                                                  |
| Pins through board | All                                                                                                                                                                                                                                                                                                                 |
| Pins routed        | 4 (GND), 5 (GND), 16 (+12V)                                                                                                                                                                                                                                                                                         |
| Board layers       | 1                                                                                                                                                                                                                                                                                                                   |

Relatively boring device. No data pins connected, just power. What's wild about
it is the IC is connected directly to 12V, so I doubt it's a microcontroller.
Its pins are a bit touchy, probably because of all the 1 megaohm resistors.
All it does is flash the amber and green LEDs back and forth.

LED pattern
-----------

Solid red, alternating amber/green at around 1.67Hz on unit measured. Not
guaranteed to be the same frequency on all units.

Photos
------

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

The IC seems to have a Toshiba logic IC pinout of sorts, with pin 4 being GND
and pin 8 being VCC. Pull pin 5 to ground, green lights; 6 to ground, amber
lights; 7 to ground, green lights stronger. Because the amber and green LEDs
are connected in series with the output in between, only one of them can light
at a time, depending on the voltage on the output.

Someone appears to have overheated the ground pins or otherwise pushed them
out of position. Not the best manufacturing.
