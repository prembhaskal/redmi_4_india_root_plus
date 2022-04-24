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
    - download tool
    - sign into your account, needs OTP from mobile
    - unlock
    - `fastboot devices` command to confirm device is properly connected.
- 
