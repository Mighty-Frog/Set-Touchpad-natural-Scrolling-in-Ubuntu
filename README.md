# Set-Touchpad-natural-Scrolling-in-Ubuntu

In Ubuntu System you may want to set merely touchpad natrual scorlling without reset mouse wheel. Unfortunately Ubuntu doesnot support that. Hence you can follow below steps to achieve it.

first input xinput list in your terminal
```
xinput list

```
you may see output like this

```
⎡ Virtual core pointer                    	id=2	[master pointer  (3)]
⎜   ↳ Virtual core XTEST pointer              	id=4	[slave  pointer  (2)]
⎜   ↳ MOSART Semi. 2.4G Wireless Mouse        	id=10	[slave  pointer  (2)]
⎜   ↳ ELAN1207:00 04F3:310E Mouse             	id=13	[slave  pointer  (2)]
⎜   ↳ ELAN1207:00 04F3:310E Touchpad          	id=14	[slave  pointer  (2)]
⎜   ↳ ELAN9009:00 04F3:29DE                   	id=15	[slave  pointer  (2)]
⎣ Virtual core keyboard    
```
find your touchpad device on the list ,my is  "ELAN1207:00 04F3:310E Touchpad"

then input following command on your termial:
```
xinput set-button-map "ELAN1207:00 04F3:310E Touchpad" 1 2 3 5 4 7 6 8 9 10 11 12

```
Then relog the account!



mouse button maps ：
1 	Left click
2 	Middle click
3 	Right click
4 	Wheel up
5 	Wheel down
6 	Wheel left
7 	Wheel right
8 	Thumb1
9 	Thumb2
10 	ExtBt7
11 	ExtBt8

