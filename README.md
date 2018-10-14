# lincomestadd
lincom, but adds results to current e() results using estadd

## Example
``` stata

clear all
sysuse auto, clear
reg mpg price foreign
lincomestadd price*1000, statname(price)
lincomestadd price*1000 + foreign, statname(priceforeign)
eststo model1

esttab model1, cells(none) stats(priceb pricese blank priceforeignb priceforeignse, label("Price" " " " " "Price+Foreign" " " " ")) noabb

```

## Installation
```
net install lincomestadd, from("https://github.com/benzipperer/lincomestadd/raw/master")
```
