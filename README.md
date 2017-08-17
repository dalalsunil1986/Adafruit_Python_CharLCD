Python + LCD (2 lines, 16 characters)
=======================

Python library to write on a LCD screen from a Raspberry Pi.
This is a modified version to work with a particular wiring of the Adafruit library available here:
https://github.com/adafruit/Adafruit_Python_CharLCD
This only takes care of the 2 lines, 16 characters, for more LCD screens make sure to head to the link above.


# 1) Wiring
| PI | LCD  | LCD Pin#  |
|---|---|---|
| GROUND  | GROUND  |  1 |
|  5V | VCC  |  2 |
| GROUND  | CONTRAST  |  3 |
| GPIO 26  | RS  |  4 |
| GROUND  | R/W  |  5 |
| GPIO 19  | ENABLE  |  6 |
| GPIO 13  | LCD D4  |  11 |
| GPIO 06  | LCD D5  |  12 |
| GPIO 05  | LCD D6  |  13 |
| GPIO 11  | LCD D7  |  14 |
| 5V  | LED+  |  15 |
| GROUND  | LED-  |  16 |

# 2) Update Your Pi
For all platforms (Raspberry Pi and Beaglebone Black) make sure you have the following dependencies:

````
sudo apt-get update
sudo apt-get install build-essential python-dev python-smbus python-pip
````

# 3) Dependency
For a Raspberry Pi make sure you have the RPi.GPIO library by executing:

````
sudo pip install RPi.GPIO
````

# 4) Install Library
### a) Clone the repo
````
git clone https://github.com/latifs/Adafruit_Python_CharLCD.git
````
### b) Install the LCD Library
````
cd Adafruit_Python_CharLCD
````
````
sudo python setup.py install
````

# 5) Try the examples
See example of usage in the examples folder.
### Ex 1 - Displays a basic 'hello world'
````
python char_lcd.py
````
### Ex 2 - Displays the IP address of the Pi
````
python char_lcd_ip_address.py
````
### Ex 3 - Displays the message passed on as an arguments on 2 lines
````
python char_lcd_custom_message.py 'Hello' 'World'
````
