# ECE Modules - Seth Freni

## Week 3 Assignment

### 5V Power Supply

The linear regulator used is the Texas Instruments LM340T-12/NOPB. The power supply requires a 0.22uF and a 0.1uF capacitor. The 0.22uF capacitor connects the input voltage (pin 1) to 
ground and is mandatory when the regulator is located far from the power supply filter. The 0.1uF capacitor is used to aid the transient response and connects from the output (pin 3)
to ground. This information was found in the
[datasheet](https://www.ti.com/lit/ds/symlink/lm340.pdf?HQS=dis-dk-null-digikeymode-dsf-pf-null-wwe&ts=1643993759861&ref_url=https%253A%252F%252Fwww.ti.com%252Fgeneral%252Fdocs%252Fsuppproductinfo.tsp%253FdistId%253D10%2526gotoUrl%253Dhttps%253A%252F%252Fwww.ti.com%252Flit%252Fgpn%252Flm340)
under "Typical Applications" on page 1, repeated on page 14. The ground pin (pin 2) connects directly to ground.

![5V PS](https://drive.google.com/uc?export=view&id=1bda3BhZU4rPVrcpSX4kY-J5_RaLv9k1V)

### 1.25-57V Adjustable Power Supply

The linear regulator used for the adjustable power supply was the ON Semiconductor LM317AHVT. The required components are a 0.1uF and 1uF capacitor, a 240 Ohm resistor (R1), and a 10k Ohm
potentiometer (R2). The 0.1uF capacitor connects the input voltage (pin 3) to ground. The 1uF capacitor connects the output voltage (pin 2) to ground. The 240 Ohm resistor connects the reference voltage (Vadj, pin 1) to the output voltage. The 10k pot connects Vadj to ground. The layout can be found on pdf page 6 (actual page 5) of the 
[datasheet](https://datasheets.diptrace.com/fairchild/lm317ahv.pdf) 
under "Typical Application". The output voltage is equal to 1.5*(1+R2/R1). There is an error factor of Iadj*R2, however this term has been deemed to small to have any effect. 

![Adjustable PS](https://drive.google.com/uc?export=view&id=1tZd24Jg9r8js5pPIXhsgAc9JQArTjn4t)

Currently the 10k pot is a placeholder as the inventory website went down as I was searching for one. The schematic will be updated when the website comes back online.
