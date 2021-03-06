# PyGPD3303S
Python interface for DC power supply GPD-3303S

## Requirements
- PySerial

## Device Driver
GPD-3303S uses a USB to serial converter chip provided by FTDI. If you have not
installed its device driver, please download and install it on your machine
first.

## Example

    >>> import gpd3303s
    >>> gpd = gpd3303s.GPD3303S()
    >>> gpd.open('/dev/ttyUSB0') # Open the device
    >>> gpd.setVoltage(1, 1.234) # Set the voltage of channel 1 to 1.234 (V)
    >>> gpd.enableOutput(True) # Output ON
    >>> v = gpd.getVoltageOutput(1) # read the actual voltage
