A place for all the non-project specific tools developed for the nRF BLE chips.

eagle/jlink_to_tag:
This contains a PCB for an adapter that converts the 20 pin JLink connector to
both a tag-connect header and a .05 inch header. Additionally, this board
supplies 3.3V to the VTRef pin on the J-Link programmer so that we can program
boards that are not self powered. To disable this, don't populate the LDO.
