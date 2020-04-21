# Pinnacle 100 Out of Box Demo (OOB Demo) Manifest Repo

## Using the OOB Demo

See the user guide for the OOB Demo [here](https://github.com/LairdCP/Pinnacle_100_oob_demo/blob/master/README.md)

## Cloning Firmware

This is a Zephyr based repository `west` manifest repository. To clone this repository properly use the `west` tool. To install `west` you will first need Python3.

Install `west` using `pip3`:

```
# Linux
pip3 install --user -U west

# macOS (Terminal) and Windows (cmd.exe)
pip3 install -U west
```

Once `west` is installed, clone this repository using `west init` and `west update`:

```
# Checkout the latest manifest on master
west init -m https://github.com/LairdCP/Pinnacle_100_OOB_Demo_Manifest.git

# OR checkout v1.0.0 tag
west init -m https://github.com/LairdCP/Pinnacle_100_OOB_Demo_Manifest.git --mr v1.0.0

# OR checkout GA1 branch
west init -m https://github.com/LairdCP/Pinnacle_100_OOB_Demo_Manifest.git --mr GA1

# Now, pull all the source described in the manifest
west update
```

### Preparing to Build

If this is your first time working with a Zephyr project on your computer you should follow the [Zephyr getting started guide](https://docs.zephyrproject.org/latest/getting_started/index.html#) to install all the tools.

It is recommended to build this firmware with the [GNU Arm Embedded Toolchain: 8-2019-q3-update](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads).

### Building the Firmware

From the directory where you issued the `west init` and `west update` commands you can use the following command to build the firmware:

```
# Windows
west build -b pinnacle_100_dvk -d oob_demo\build oob_demo\oob_demo

# Linux and macOS
west build -b pinnacle_100_dvk -d oob_demo/build oob_demo/oob_demo
```
