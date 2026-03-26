# OvoEasy PCB through-hole assembly

To reduce costs, you may choose to order your OvoEasy boards with only SMD components assembled. In this case, you will need to populate remaining through-hole components by hand.


## Through-hole parts BOM


| Reference | Value | Qty | MPN | LCSC | Description | Mouser | LCSC |
|---|---|---|---|---|---|---|---|
| DC1 | DC007B-2.0 | 1 | PJ-106AH-TR | C17701683 | DC barrel jack, 2.0mm pin, TH | [Mouser](https://www.mouser.com/ProductDetail/Same-Sky/PJ-106AH-TR) | [LCSC](https://www.lcsc.com/product-detail/C17701683.html) |
| J3 | Conn_01x04 | 1 | 1984989 | — (alt: C475156, Kefa KF250-3.5-4P-1) | Phoenix PTSA 1.5/4, 4-pos 3.5mm push-in terminal block | [Mouser](https://www.mouser.com/ProductDetail/Phoenix-Contact/1984989) | [LCSC alt](https://www.lcsc.com/product-detail/C475156.html) |
| J4 | Conn_01x04_Socket | 1 | 04JQ-ST | C2897386 | JST JQ 4-pin receptacle, 2.5mm pitch, right-angle TH | [Mouser](https://www.mouser.com/ProductDetail/JST/04JQ-ST) | [LCSC](https://www.lcsc.com/product-detail/C2897386.html) |
| J5 | Conn_01x06 | 1 | B6B-PH-K-S(LF)(SN) | C131342 | JST PH 6-pin vertical header, 2.0mm pitch | [Mouser](https://www.mouser.com/ProductDetail/JST-Commercial/B6B-PH-K-SLFSN) | [LCSC](https://www.lcsc.com/product-detail/C131342.html) |
| J6, J13 | Conn_01x04 | 2 | B4B-PH-K-S(LF)(SN) | C131334 | JST PH 4-pin vertical header, 2.0mm pitch | [Mouser](https://www.mouser.com/ProductDetail/JST-Commercial/B4B-PH-K-SLFSN) | [LCSC](https://www.lcsc.com/product-detail/C131334.html) |
| J7 | Conn_01x04 | 1 | TBP02R2-381-04BE | — (alt: C395697, DORABO DB2EVC-3.81-4P-GN) | CUI/Same Sky 4-pos pluggable terminal block header, 3.81mm pitch | [Mouser](https://www.mouser.com/ProductDetail/CUI-Devices/TBP02R2-381-04BE) | [LCSC alt](https://www.lcsc.com/product-detail/C395697.html) |
| J7 plug | — | 1 | TBP02P1-381-04BE | — (alt: C395699, DORABO DB2EK-3.81-4P-GN-S) | 4-pos mating plug for J7, 3.81mm pitch | [Mouser](https://www.mouser.com/ProductDetail/CUI-Devices/TBP02P1-381-04BE) | [LCSC alt](https://www.lcsc.com/product-detail/C395699.html) |
| J8, J9 | Conn_01x03 | 2 | B3B-PH-K-S(LF)(SN) | C131339 | JST PH 3-pin vertical header, 2.0mm pitch | [Mouser](https://www.mouser.com/ProductDetail/JST-Commercial/B3B-PH-K-SLFSN) | [LCSC](https://www.lcsc.com/product-detail/C131339.html) |
| J10 | Conn_01x03 | 1 | B3B-XH-A(LF)(SN) | C144394 | JST XH 3-pin vertical header, 2.5mm pitch | [Mouser](https://www.mouser.com/ProductDetail/JST-Commercial/B3B-XH-ALFSN) | [LCSC](https://www.lcsc.com/product-detail/C144394.html) |
| J11, J12, J14 | Conn_01x02 | 3 | B2B-PH-K-S(LF)(SN) | C131337 | JST PH 2-pin vertical header, 2.0mm pitch | [Mouser](https://www.mouser.com/ProductDetail/JST-Commercial/B2B-PH-K-SLFSN) | [LCSC](https://www.lcsc.com/product-detail/C131337.html) |
| SW2 | RotaryEncoder_Switch | 1 | EC12D1524403 | C112349 | Alps Alpine 15-pulse rotary encoder w/ push switch, TH | [Mouser](https://www.mouser.com/ProductDetail/Alps-Alpine/EC12D1524403) | [LCSC](https://www.lcsc.com/product-detail/C112349.html) |

**Notes:**
- J3 and J7 primary MPNs are not stocked on LCSC; alternative parts are noted parenthetically in the LCSC column.
- The J7 mating plug (wire-side) is listed as a 

## Assembly

This is one recommended order to help you go through the assembly. Steps are grouped in parts of similar height spread across the board, which can help with the 'balance things on a flat surface' approach. Alternatively, you could make a printed jig for assembly of all components on a side at once. Make sure to use good soldering supplies and technique to ensure quality joints.

If not using a jig, you may find it useful to add small dabs of hot glue to the plastic housings of some components to help them stay in place when flipping the board to solder the leads. If you do this, make sure not to obstruct the connector path with glue.

### Step 1: Pin headers

<img src='./Images/Step01_pinheaders.png' width=600>

Standard 2.54mm female pin headers are used to connect the LCD display and the water atomizer board. You can also optionally use a 9-pin header here -- the remaining 5 pins (for touch-screen functionality) are unused. 

The USB-C always-on atomizer boards can have headers in different orientations. Solder 2-pin female headers in both spots for maximum flexibilty. You will need to also solder male headers onto the the atomizer boards -- make sure the installed pins face up (same side as atomizer board components); these are meant to be installed 'upside down'.

### Step 2: DC in and JST-XH

<img src='./Images/Step02_JST-DC.png' width=600>

Next, install the 3-pin JST-XH header for the water level sensor and the DC barrel jack. 

Make sure the JST header is installed so that the pins match your particular sensor, or re-pin the sensor to match the board.

### Step 3: remaining front-side components

<img src='./Images/Step03_otherfront.png' width=600>

Finally, install the remaining front-side components: the terminal block, the encoder, and (if using) the W5500 ethernet module. 

The encoder can be a little tough to push into its footprint, as it has stiff mechanical connectors to help lock it in place. Make sure to give these mechanical connectors plenty of solder.

### Step 4: back-side JST-PH headers

<img src='./Images/Step04_backJST.png' width=600>

Now, flip the board and install the JST-PH headers on the back side. There are three two-pin, two three-pin, two four-pin, and one six-pin headers.

### Step 5: remaining back-side components

<img src='./Images/Step05_otherback.png' width=600>

Finally, install the 5mm pluggable terminal block connector for the fan/heater module, and the female 2.54mm header for the environmental sensor module. 

The 04JQ-ST connector from JST (illustrated above) mates with a four-pin JST-XH connector, and will provide positive retention of the module. You can also use a standard four-pin 2.54 female header here instead.