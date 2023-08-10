# Bootstrap

Bootstrap link comes before CSS link.

Rows and colums have to exist inside a container. If you dont do it then the rows extend past the width of the browser. Youll get side scroll.

All bootstrap stuff must be in a container. ⭐
                     |
                    \ /
Fluid container wraps to the full width of the browser.
container-fluid ⭐⭐⭐

display: flex; flex-wrap: wrap;


Makes rows sections and col a div for better organization.

Columns will evenly distribute thru row.

Columns can be given an exact size 1-12. Columns will add up to 12. Adjust size of other columns when changing another.

Always have a base column size without infix.
  |
 \ /
col-6 - default   col-md-4 - will be 4 on medium screens and larger
                      / \
                       | that is an infix
use infixes for responsive design ⭐⭐⭐
use col-12 as base size for mobile friendly sites, bigger col size for smaller screens ⭐

can use infixes on padding and margin and other stuff ⭐

d-lg-none - for example will hide something on a screen larger than 900px ⭐

you can re order html with flex/bootstrap by using order-first for default and then order-md-last

Rows are d-flex by default

text-end to align text all the way to the right of the column

Offset creates margin equal to the width of a col ⭐⭐

Margin takes up space in a row/column on the x and y axis and makes row/col bigger

Padding doesnt add onto the size

No right and left in bootstrap, only start and end, STBE and X and Y at the end of P/M⭐⭐

M is margin P is padding ex: p-3 m-2

img-fluid makes images fit into whatever container theyre in
text-center on div will center image ⭐⭐

Text center header and then text-start paragraph

text-md-center - breakpoint for text align