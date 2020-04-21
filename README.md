# KBD-USB2PS2

![kbd-usb2ps2](kbd-usb2ps2.png)

This program makes the conversion of the USB HID keyboard protocol to the PS/2 keyboard protocol (scan code set 2).

The original ideal of this program is from [usb2ps2](https://github.com/limao693/usb2ps2), but it didn't realize **typematic rate** and  **typematic delay** and the *USB Host Shield* library it used is too old. So this program fix the all problems above.

## Hardware Requirements

* Arduino Uno Rev3
* USB Host Shield V2.0

## Usage

1. Install [Arduino IDE](https://www.arduino.cc/en/Main/Software)
2. Install [USB Host Shield Library 2.0](https://github.com/felis/USB_Host_Shield_2.0) in Arduino IDE
3. Brush this program (kbd-usb2ps2.ino) into Arduino Uno Rev3
4. Assemble USB Host Shield V2.0 on Arduino Uno Rev3
5. Connect PS/2 **data line** and **clock line** to Arduino (**4**, **2**)

:warning: Note: You should plug PS/2 into computer before the computer is turned on, because PS/2 does not support [hotplugging](https://en.wikipedia.org/wiki/PS/2_port#Hotplugging).

## Compatiable Keyboard

:heavy_check_mark: : Support, :x: : Not Support

* HHKB Professional Type-S :x:
* CHERRY G80-3494LWCEU-0 :heavy_check_mark:
* ...

It seems USB Host Shield V2.0 don't support USB keyboard with internal hub, so if your keyboard has internal hub, it won't work.

:rose: Welcome PR to contribute to this keyboard support list.

## TODO

* [ ] Num Lock key not working
* [x] BIOS boot checking not recognize this program as a PS/2 keyboard

## Reference

* [The PS/2 Mouse/Keyboard Protocol](https://www.avrfreaks.net/sites/default/files/PS2%20Keyboard.pdf), Adam Chapweske
* [USB HID to PS/2 Scan Code Translation Table](https://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/translate.pdf), Microsoft
