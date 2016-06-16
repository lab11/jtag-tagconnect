JTAG to Tag Connect
===================

This PCB is an adapter that converts the [20 pin JLink](https://www.segger.com/jlink-debug-probes.html) connector to
a [6-pin Tag Connect](http://www.tag-connect.com/TC2030-IDC-NL),
much like [this](https://www.segger.com/jlink-6-pin-adapter.html) board.
Ours, however, additionally contains an onboard LDO
that can supply 3.3V to the attached device and the VTRef pin on the J-Link programmer
so that it can program boards that are not self powered.

Interface
---------

- **Switch 1**, labeled `VREF`: Set to `3V3` to connect the `VCC` pin on the TagConnect
header (and the attached board to be programmed) and the `VTRef` pin from
the Segger JLink to the 3.3 V output from the regulator.
Set to `DEV` to directly connect the `VTRef` pin on the JLink to the TagConnect
VCC pin. This sets the I/O voltage for the JLink, but does not power the target board.

- **Switch 2**, labeled `SWDIO`: This switch can connect the `SWDIO` and
`!RESET` signals, which is needed on some ICs. To leave the signals
disconnected, leave the switch in the empty (down) position.


Troubleshooting
---------------

1. Blue LED does not come on when attached to JLink.
You need to enable the 5 V output on the JLink:

        $ JlinkExe
        power on perm
