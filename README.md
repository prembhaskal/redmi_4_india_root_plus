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
- install SuperSU and lazyflasher
  - follow  youtube link - https://www.youtube.com/watch?v=ppoJYB2gfLg 
  - download latest flashable super su from here - http://supersuroot.org/downloads/SuperSU-v2.82-201705271822.zip 
    - also downloaded here - https://drive.google.com/file/d/10NQKLRBSsRTBVhgeJsfQxs3pVIYh8_SY/view?usp=sharing 
  - downloaded lazyflasher - https://drive.google.com/file/d/1ZFEuzBBvFny_5-SnZOL0rHKpiUxBolP4/view or https://drive.google.com/file/d/1mXWO84u3YwDyCGHwhO1Ibc_xsm9_9AbC/view?usp=sharing 
  - boot phone into TWRP recovery if not already done.
  - TWRP wipe data
  - copy the supersu and lazyflasher zip into the SDCard of phone, phone will be visible in PC to transfer data. Alternatively adb push commands can be used if phone is not visible.
  - TWRP > install > supersu zip > flash
  - TWRP > install > lazyflasher zip > flash (might show error, ignore it)
  - TWRP > reboot > system
- check root access for first time
  - first time login might ask to enter MI account password.
  - SuperSU app will be installed, otherwise download and install
  - install rootchecker from playstore, grant permissions in supersu app, run root check.
