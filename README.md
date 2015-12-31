# OpenDeck MIDI Platform

OpenDeck is a platform for building DIY MIDI controllers. Connect your potentiometers, buttons, LEDs and other stuff your want in your MIDI controller
to OpenDeck board and start using your new MIDI controller in no-time. Compatible with any MIDI software on any OS.

## Repository content
* Firmware
* Bootloader
* Part list
* Configuration documentation
* Schematic (PDF)
* PCB files (gerbers)

# Configurable features

### MIDI channels

* Note
* Program change
* Control change
* Pitch bend
* MIDI input

### MIDI settings

* Enable/disable standard note off
* Enable/disable running status (DIN MIDI only)
* Enable/disable DIN MIDI in to USB MIDI out converter

### Button configuration

* Button type (momentary/latching)
* Enable/disable program change send instead of notes
* MIDI note

### Analog configuration

* Enable/disable analog input
* Invert analog value
* Analog input type
* CC number
* Lower CC limit
* Upper CC limit

### LED configuration

* Hardware parameters:
  - total LED number
  - blink time
  - start-up LED switch time
  - start-up animation routine
  - fade speed
* LED activation note
* LED start-up number
* Enable/disable RGB LED
* Test LED state

### Encoder configuration

* Enable/disable encoder
* Invert encoder value
* Encoding type
* CC number

### Data restoration

* Restoration of single parameter back to default (ie. restore potentiometer 6 CC number to default)
* Restoration of all parameters within message type (ie. restore all button notes to default)
* Complete factory reset of all values

### SysEx configuration
All configuration is done using MIDI System Exclusive messages. For more information, see `configuration.md` in `doc` directory.

### Firmware update

OpenDeck uses LUFA mass storage bootloader for firmware updating. For more information on how to update firmware, see `firmware_update.md` in `doc` directory.

## Firmware compilation
MCU Code is available as Atmel Studio 7.0 project. Simply open `OpenDeck_AVRC.atsln` using the IDE and everything should work.

## Credits

Hardware MIDI source code based on [Arduino MIDI library v3.2](https://github.com/FortySevenEffects/arduino_midi_library/releases/tag/3.2) by Francois Best.

USB MIDI source code based on [Teensyduino Arduino add-on](http://www.pjrc.com/teensy/teensyduino.html) by Paul Stoffregen and PJRC.com LLC.

Parts of code taken from [Arduino framework](https://github.com/arduino/Arduino).

Bootloader code based on [LUFA Mass Storage bootloader](http://www.fourwalledcubicle.com/LUFA.php) by Dean Camera.

## Licence
All code is available under GNU GPL v3 licence.