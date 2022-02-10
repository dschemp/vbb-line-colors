# vbb-line-colors

I used https://www.ralfarbpalette.de/ral-classic and
https://color.adobe.com/de/create/color-contrast-analyzer to determine the hex color
from the RAL color given by the VBB and to determine the text color.

`alternate-colors.json` uses the Wikipedia's hex colors for some of the transit types and all the subway lines.


## Format

The colors are sorted by the type of transit like `subway`, `tram` and `regional`.
There is not distinction between Metro and normal Tram/Bus or Regional and Regional Express.

Each type of transit contains the line numbers as their display name like `.suburban.S2` instead of `.suburban.2`.

Each line contains a foreground (`fg`) and background (`bg`) color in hex format (without `#`).
Some include a RAL number.

Default transit type colors are defined under `_default`.
They can be used instead of line specific colors or when a line is not included.
Included is an `unknown` type which is just græy.

Ferries and (Metro)Busses are supposed to use the default colors.
There exists a Bus and Ferry map by the BVG for routes in* Berlin but these colors are too uncommon in real life.


## Sources

- https://de.wikipedia.org/wiki/Berliner_Verkehrsbetriebe#Farben
- https://www.vbb.de/vbb-services/api-open-data/datensaetze/
- https://www.bvg.de/en/connections/network-maps-and-routes
- https://github.com/derhuerst/vbb-logos


## My Critic

IT IS FREAKIN' HARD finding the right colors for display as the RAL colors are somewhat
standardised but the conversion to hex is different everytime you blink.

The hex colors given by the VBB in the [Open Data's Line Color](https://www.vbb.de/vbb-services/api-open-data/datensaetze/) CSV
are basically all off and look bad (and they are missing text colors). 

[S-Bahn Berlin](https://sbahn.berlin) seems to use different colors for their website than what I could determine.
S45, S46 and S47 should be the same color according to VBB (RAL 1011) but S45 is different. thx

BVG seems to provide color codes / corporate design stuff somehow (according to a Wikipedia reference) but nothing is publicly available.
Imagine the fun having to use the Snipping tool and paint.net to extract colors from the Tram map.

**TL;DR:** It's a total mess.
