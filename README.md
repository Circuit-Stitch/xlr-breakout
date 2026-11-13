# XLR breakout

Single-channel balanced breakout boards. Each board holds one XLR jack. Use one board per channel. The
jack fits a D-series panel cutout. Each board is 27.6 mm square and hangs on its jack behind the panel.

A JST PH 4-pin header (B4B-PH-K) sits on the back of the board. The cable leaves toward the rear of the
enclosure.

| Pin | Signal | XLR | 1/4" TRS (female only) |
| --- | --- | --- | --- |
| 1 | HOT | Pin 2 | Tip |
| 2 | COLD | Pin 3 | Ring |
| 3 | 0V | Pin 1 | Sleeve |
| 4 | CHASSIS | G | — |

Pins 1 to 3 match the JST PH 3-pin line-out connectors on DOAT dat_main (HOT, COLD, GND). A straight PH
cable works.

Pin 4 carries the XLR shell contact (G). Bond it to the chassis on the audio board. It is not connected
to 0V on these boards.

The jack switch contacts (TN, RN, SN) are not connected. T and R are tied to XLR pins 2 and 3, so
grounding TN or RN would short the XLR signal when only an XLR plug is in.

## Order

Both boards are shared on OSH Park.

| Board | Order |
| --- | --- |
| Female, rev 3 | <a href="https://oshpark.com/shared_projects/ie4ZloEW"><img src="https://oshpark.com/assets/badge-5b7ec47045b78aef6eb9d83b3bac6b1920de805e9a0c227658eac6e19a045b9c.png" alt="Order from OSH Park"></a> |
| Male, rev 1 | <a href="https://oshpark.com/shared_projects/khsZ1jXg"><img src="https://oshpark.com/assets/badge-5b7ec47045b78aef6eb9d83b3bac6b1920de805e9a0c227658eac6e19a045b9c.png" alt="Order from OSH Park"></a> |

## Layout

| Folder | Contents |
| --- | --- |
| `breakout-female/` | Input board. One REAN RCJ9FA-V XLR and 1/4" TRS combo jack. Rev 3. |
| `breakout-male/` | Output board. One REAN RRX3M-AA-003-0 male XLR jack. Rev 1. |
| `lib/` | Shared footprints, symbol, 3D model, and datasheets. Both projects load it through `${KIPRJMOD}/../lib`. |

Female rev 1 to rev 2 were two-jack boards with a 6-pin 2.54 mm header (0V, L+, L−, 0V, R+, R−) and G
on 0V. `breakout-female/gerbers/` holds the zip sent to the fab for each of those revisions. This
project was `dat_alpha` in the DOAT repo.
