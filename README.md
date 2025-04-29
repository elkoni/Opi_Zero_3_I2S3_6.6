# Opi_Zero_3_I2S3_6.6
Orange PI Zero 3 Armbian v25.02 Kernel 6.6.72 I2S audio output 

  This is set of patches to enable I2S audio output on Armbian v25.02 on OrangePi Zero 3 ( H618 SoC ).  
They are placed in "userpatches/kernel/archive/sunxi-6.6" directory.  
  I am using Armbian stable branch with kernel 6.6.72.  
    git clone --depth=1 --branch=v25.02 https://github.com/armbian/build  
  The following bitrates are tested 16000,22050,32000,44100,48000,88200,96000,176400 and 192000.  
Seems, that driver ( sunxi_v2 ) uses only 32 bit slots for I2S, so the BCLK is the same for any  
bith depth ( 16, 24 or 32 ).  
You will need an i2s3 overlay from Opi_Zero_3_I2S3_6.1 repo.  
Patches 001 and 002 may be combined or added as overlay. 

Based on work from https://forum.armbian.com/topic/37718-sound-on-h616h618-socs/ and many trials and  
errors ( because i am altered kernel config too - not related to i2s ).  
Patch 004 is not related to I2S output. It adds usb0-host overlay, used to boot from USB storage device. 


  







