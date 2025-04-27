# Opi_Zero_3_I2S3_6.6
Orange PI Zero 3 Armbian v25.02 Kernel 6.6.72 I2S audio output 

This is set of patches to enable I2S audio output on Armbian v25.02 on OrangePi Zero 3 ( H618 SoC ).  
They are placed in "userpatches/kernel/archive/sunxi-6.6" directory.  
I am using Armbian stable branch with kernel 6.6.72.  
git clone --depth=1 --branch=v25.02 https://github.com/armbian/build  
  The following bitrates are tested 16000,22050,32000,44100,48000,88200,96999,176400 and 192000.  
Seems, that driver ( sunxi_v2 ) uses only 32 bit slots for I2S, so the BCLK is the same for any  
bith depth ( 16, 24 or 32 ).







