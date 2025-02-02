ARM Cortex-M3 BOOTROM from Huawei E5885 (Balong v7r22, Hi6932)
Load address: 0x1FFE0000
Thumb-2 mode only.

Dumped with raminit exploit, because m3 monitor doesn't have access to 0x1FFE0000.
Raminit return to bootrom address (lr) = 0x1ffe29dd

HI_BOOTROM_REGBASE_ADDR 0x200F0000 is INCORRECT!

UART configuration:
stty -F /dev/ttyUSB0 raw 115200 -echo -echoe -echok



To temporary disable Secure Boot, execute 0x1FFE5C54 function.
