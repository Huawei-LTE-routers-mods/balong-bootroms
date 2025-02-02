ARM Cortex-M3 BOOTROM from Huawei E6878 router (Balong 5000).

Load address: 0x80000
Thumb-2 mode only.


return address from 0xDA protocol packet: 0x7cb24

The best exploit it to write address to 0x07cb08 (address on bootrom's stack), which originally points to 0x80D01 (very simple function).

Other execution candidates:
0x07cb1c
0x07cb0c

To temporary disable Secure Boot, execute 0x00084A18 function.

The same bootrom is also found on H122 device.




I've acidentally switched my device to CryptoCell Security Lifecycle States (LCS) = 7 Return Merchandise Authorization (RMA), as far as I remember, this was because I did not populate SRAM values, which crashed the firmware boot process, and patched the place it has crashed, allowing it to continue.

Turns out the "continue" code was burning efuses into RMA state :P
