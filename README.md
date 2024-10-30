# Q-SYS-Bose-VB1-Videobar-REST API

- Bose VB1 Q-Sys Plugin (REST API)
- Written by Glen Gorton (glen.gorton@gmail.com)
- Tested with Firmware version 1.5.1_75ebaa7

## NOTES:
- Disconnect Bluetooth Device' -- bluetooth.disconnect (1.3.6.1.4.1.6036.727.228)
REST API has the ability to send Values 1, 2 or 3 but no information on what these do. Found 1 and 3 will disconnect the currently connected bluetooth device, and 2 will do nothing.
'Bluetooth Disconnect Device' EventHandler is sending a Value of 1.

- 'USB Call Status'
MS Teams and Zoom must have Bose VB1 selected as the microphone in order for the response to be true ("1"). Tested with Zoom Workplace Version: 6.1.1 (41705) and Microsoft Teams version 24165.1414.2987.41.

- 'System Name'
Device loses connectivity when system.name is changed via SNMP, REST API or HTTP interface. SNMP Guide documents says "Reboot on Update: no".
When changing name via HTTP interface a prompt warns the device will reboot. Informed Bose of incorrect documentation.
Script functions as if the Reboot function has been triggered, setting Status to Initialzing - Device Rebooting...
