# ML8511
This repo contains the slope line estimation for GY-ML8511 UV sensor for Arduino Uno

Followng is the OUTPUT VALTAGE– UV INTENSITY CHARCTERISTICS from the LAPIS datasheet (https://cdn.sparkfun.com/datasheets/Sensors/LightImaging/ML8511_3-8-13.pdf)
![Screenshot from 2023-08-22 11-57-25](https://github.com/ParthaPRay/ML8511/assets/1689639/908cc1df-b504-478a-ad76-4a805d0a2857)

From the above plot we can estimate the relationship between UV intensity (mW/cm<sup>2</sup>) and output voltage (V) as follows.

We try to estimate m i.e. sole of the straight line from the above plot.

(y<sub>2</sub> - y<sub>1</sub>) = m (x<sub>2</sub> - x<sub>1</sub>)       equation (1)

Where:
x<sub>1</sub> = 0, y<sub>1</sub> = 1.0

x<sub>2</sub> = 10, y<sub>2</sub> = 2.2

Thus, 

m = (y<sub>2</sub> - y<sub>1</sub>)/(x<sub>2</sub>-x<sub>1</sub>)

m = (2.2 - 1.0)/(10 - 0)

m = 0.12


So, the final formula can be written as below:

O/P Voltage = (0.12 * UV Intensity) + 1


