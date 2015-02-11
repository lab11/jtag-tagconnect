nRF51*** Tools
==============

A place for all the non-project specific tools developed for the nRF BLE chips.

JLink to Tag Connect Adapter
----------------------------
This PCB is an adapter that converts the [20 pin JLink](https://www.segger.com/jlink-debug-probes.html) connector to
a [6-pin Tag Connect](http://www.tag-connect.com/TC2030-IDC-NL),
much like [this](https://www.segger.com/jlink-6-pin-adapter.html) board.
Ours, however, additionally contains an onboard LDO
that can supply 3.3V to the attached device and the VTRef pin on the J-Link programmer
so that it can program boards that are not self powered. To disable this, put the switch
in the "Device" setting.
