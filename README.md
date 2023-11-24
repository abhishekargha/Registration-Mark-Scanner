# Registration-Mark-Scanner
My bot is a portable device which can be used in flexographic printing machines which uses “registration marks" to ensure proper alignment throughout the printing process of any package. It helps quality teams solve issues such as if the machine needs to be recalibrated or reset the tension control according to the printing substrate or reduce drying temperature etc.
It uses a microcontroller (Arduino or Raspberri pi) and an RGB color sensor (TCS230 or TCS3200). The RGB color sensor has an oscillator that outputs frequency in the form of square wave based on the wavelength of the incident light on the photodiodes. The output square wave frequency is later used to detect the RGB content of colour to define object colour.
First we teach the microcontroller to recognize which frequency range as which color. To do so we feed different colors to the sensor and as the serial monitor shows the rise in the output frequency, we record that.
Next we use those recorded frequencies as parameters for detecting the color of objects that incur frequencies within that range when incident on the RGB sensor in the future.
Now this “almost” smart bot can be set up on any printing machine and for final teaching, we need to assign a value to the function “delay ()” which we use extensively in the code. The unit is in nanoseconds (a great property to have when dealing with high-speed printing machines)and the value depends on the time it takes for one batch of registration marks to pass through a certain point on the printing machine.