# redmi_4_india_root_plus

## How I rooted my Redmi4 (india version) phone and installed linux on it.

- unlock bootloader
  - link: https://www.guidetoroot.com/unlock-bootloader-on-any-xiaomi-phones/
  - on phone
    - enable developer options.
    - developer option - long press OEM unlock , enter screen lock and enable OEM unlock
    - developer option - enable USB debugging
    - developer option - MI unlock status, add account and device. Note this needs mobile data connectivity.
    - power off
    - boot into fastboot.
  - On PC
    - Install USB drivers from here https://flashxiaomi.com/xiaomi-redmi-4-usb-driver/ 
  - MI unlock tool
    - download tool - used software - miflash_unlock-en-6.5.406.31.zip
      - shared download link https://drive.google.com/file/d/14w5n7_8Ya-yw7l_A1eQ8edJRNLHbrJ2Y/view?usp=sharing 
    - sign into your account, needs OTP from mobile
    - unlock
    - `fastboot devices` command to confirm device is properly connected.
- install TWRP recovery
  - download TWRP santoni https://dl.twrp.me/santoni/twrp-3.6.0_9-0-santoni.img.html
    - also downloaded here - https://drive.google.com/file/d/1Ii08ZDtJgpwRdRSeOeW5VV_TSKXfs5HZ/view?usp=sharing
  - copy to miflash_unlock-en-6.5.406.31/ directory and rename to recovery.img
  - run below commands to flash the TWRP 
  ```
  fastboot devices
  fastboot flast recovery recovery.img
  fastboot reboot recovery
  ```
  - now phone will be booted into TWRP recovery
  - 
  
