ecoOBD2 (2022-09)
=================

|                    |                                                                                                                                                                                                                                                      |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name               | ecoOBD2 (Diesel)                                                                                                                                                                                                                                     |
| Purchase date      | 2022-09                                                                                                                                                                                                                                              |
| Color              | Blue                                                                                                                                                                                                                                                 |
| Purchase link      | [eBay](https://www.ebay.com/itm/353104715188?var=622307849279), seller [smart-alice](https://www.ebay.com/str/moduleimage)<br>[eBay](https://www.ebay.com/itm/185419495356?var=693214925853), seller [soldity88](https://www.ebay.com/str/soldity88) |
| Type               | Analog flasher, non-connected                                                                                                                                                                                                                        |
| Power draw         | Unmeasured (power source not 12V)                                                                                                                                                                                                                    |
| MCU                | N/A                                                                                                                                                                                                                                                  |
| Pins through board | 4 (GND), 5 (GND), 6 (CAN high), 7 (K-Line), 8 (disc.), 14 (CAN low), 15 (L-Line), 16 (+12V)                                                                                                                                                          |
| Pins routed        | 4 (GND), 5 (GND), 16 (+12V)                                                                                                                                                                                                                          |
| Board layers       | 2                                                                                                                                                                                                                                                    |

This one is using a simple astable multivibrator to blink one LED while leaving
two other LEDs always lit. No connection to busses.

Big Clive did a teardown of this design [here](https://www.youtube.com/watch?v=axow7KnBtaM).

LED pattern
-----------

Solid red and green, amber blink on for ~0.25s, off for ~0.75s.

Sample 1
========

Photos
------

<table>
<tbody>
<tr>
<td><a href="1/packaging/package_front.jpg"><img src="1/thumbs/package_front_t.jpg" alt="Package front"></a></td>
<td><a href="1/packaging/package_back.jpg"><img src="1/thumbs/package_back_t.jpg" alt="Package back"></a></td>
</tr>
</tbody>
</table>

Not even any packaging, just a bag. I'm disappointed.

### Device shell

<table>
<tbody>
<tr>
<td><a href="1/shell/front.jpg"><img src="1/thumbs/front_t.jpg" alt="Shell front"></a></td>
<td><a href="1/shell/back.jpg"><img src="1/thumbs/back_t.jpg" alt="Shell back"></a></td>
</tr>
<tr>
<td><a href="1/shell/top.jpg"><img src="1/thumbs/top_t.jpg" alt="Shell top"></a></td>
<td><a href="1/shell/bottom.jpg"><img src="1/thumbs/bottom_t.jpg" alt="Shell bottom"></a></td>
</tr>
<tr>
<td><a href="1/shell/left.jpg"><img src="1/thumbs/left_t.jpg" alt="Shell left"></a></td>
<td><a href="1/shell/right.jpg"><img src="1/thumbs/right_t.jpg" alt="Shell right"></a></td>
</tr>
</tbody>
</table>

### Board

<a href="1/board/board.jpg"><img src="1/thumbs/board_t.jpg" alt="Board"></a>

Sample 2
========

Photos
------

<table>
<tbody>
<tr>
<td><a href="2/packaging/package_front.jpg"><img src="2/thumbs/package_front_t.jpg" alt="Package front"></a></td>
<td><a href="2/packaging/package_back.jpg"><img src="2/thumbs/package_back_t.jpg" alt="Package back"></a></td>
</tr>
<tr>
<td><a href="2/packaging/insert_front.jpg"><img src="2/thumbs/insert_front_t.jpg" alt="Insert front"></a></td>
<td><a href="2/packaging/insert_back.jpg"><img src="2/thumbs/insert_back_t.jpg" alt="Insert back"></a></td>
</tr>
<tr>
<td><a href="2/packaging/insert_inside_top.jpg"><img src="2/thumbs/insert_inside_top_t.jpg" alt="Insert inside top"></a></td>
<td><a href="2/packaging/insert_inside_bottom.jpg"><img src="2/thumbs/insert_inside_bottom_t.jpg" alt="Insert inside bottom"></a></td>
</tr>
</tbody>
</table>

### Device shell

<table>
<tbody>
<tr>
<td><a href="2/shell/front.jpg"><img src="2/thumbs/front_t.jpg" alt="Shell front"></a></td>
<td><a href="2/shell/back.jpg"><img src="2/thumbs/back_t.jpg" alt="Shell back"></a></td>
</tr>
<tr>
<td><a href="2/shell/top.jpg"><img src="2/thumbs/top_t.jpg" alt="Shell top"></a></td>
<td><a href="2/shell/bottom.jpg"><img src="2/thumbs/bottom_t.jpg" alt="Shell bottom"></a></td>
</tr>
<tr>
<td><a href="2/shell/left.jpg"><img src="2/thumbs/left_t.jpg" alt="Shell left"></a></td>
<td><a href="2/shell/right.jpg"><img src="2/thumbs/right_t.jpg" alt="Shell right"></a></td>
</tr>
</tbody>
</table>

The "Nkaay" logo is aligned top instead of bottom.

It was actually a little difficult to get into this one because the back piece
was slightly sticking out compared to the front shell, so I had to try to stick
the spudger in from a corner rather than pull on the shell with my nails as I
usually could.

### Board

<a href="2/board/board.jpg"><img src="2/thumbs/board_t.jpg" alt="Board"></a>

Same board layout, but ever so slightly different silkscreen. The clearance
around vias is also a bit different. This suggests someone probably used a
PCB layout file instead of just submitting Gerbers, and maybe project files
are making the rounds.

Schematic
---------

![Schematic](1/board/schematic.png)

Just an astable multivibrator made of discrete components, nothing too amazing.
That fuse is just a 0-ohm resistor. Good of them to have considered a fuse, at
least?
