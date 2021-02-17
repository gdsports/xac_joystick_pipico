# USB Joystick using Raspberry Pi Pico and TinyUSB

This based on modifications to the dev_hid_composite example from the
pico-examples repo.

## How to build on a Raspberry Pi

```bash
cd ~/pico
git clone https://github.com/gdsports/xac_joystick_pipico
cd xac_joystick_pipico
mkdir build
cd build
export PICO_SDK_PATH=../../pico-sdk
cmake ..
make -j4
```
