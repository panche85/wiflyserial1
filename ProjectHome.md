WiflySerial1 is a library designed to work with the Arduino Mega 2560 or the Arduino Due.

It communicates with the WiFly Shield from Sparkfun Electronics through serial port Serial1

It is highly inspired from the library WiFlySerial written by Tom Waldock.
WiFlySerial is more complete but use SoftwareSerial witch is hardware dependant and don't work with Arduino Due.

WiflySerial1 need the libraries PString and Streaming than can be found at http://arduiana.org

Connection between Arduino Due (or Mega 2560) and WiFly consist in 4 wires:

> Arduino GND to WiFly GND
> Arduino 3V3 to WiFly 3.3V-RIN
> Arduino RX1 (19) to WiFly TX
> Arduino TX1 (18) to WiFly RX

Example sketch WiflySerial1Test do not use the WiflySerial1 library.
The purpose of this sketch is to test the physical connections  between Arduino and Wifly and to play with Wifly set of commands (see the manual of WiFly RN-131 for reference at http://ww1.microchip.com/downloads/en/DeviceDoc/rn-wiflycr-um-1.0r.pdf?from=rss ).

Example sketch WiflyWebTimeServer show how to use the WiflySerial1 library to implement a web server.
A good way to understand how the library works is to load the sketch WiflyWebTimeServer in your ide or any editor and to search for any appearance of wifi object.

Be aware than setting WiFly uart baudrate to value different from 9600 bauds can result in difficulties to recover the default baudrate. So do not modify the instruction wifi.begin() until you know what you are doing!

Remember to check voltage applied to Wifly module before powering the circuit (must be 3,3 Volt).