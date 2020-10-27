# Pinnacle 100 Out of Box Demo (OOB Demo) Manifest Repo

## Using the OOB Demo

See the user guide for the OOB Demo [here](https://github.com/LairdCP/Pinnacle_100_oob_demo/blob/master/README.md)

## Cloning Firmware

This is a Zephyr `west` manifest repository. To learn more about `west` see [here](https://docs.zephyrproject.org/latest/guides/west/index.html).

To clone this repository properly use the `west` tool. To install `west` you will first need Python3.

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

# OR checkout v3.0.0 tag
west init -m https://github.com/LairdCP/Pinnacle_100_OOB_Demo_Manifest.git --mr v3.0.0

# OR checkout GA3 branch
west init -m https://github.com/LairdCP/Pinnacle_100_OOB_Demo_Manifest.git --mr GA3

# Now, pull all the source described in the manifest
west update
```

## Preparing to Build

If this is your first time working with a Zephyr project on your computer you should follow the [Zephyr getting started guide](https://docs.zephyrproject.org/latest/getting_started/index.html#) to install all the tools.

The OOB demo uses zephyr 2.3.x, so GCC 9 is recommended.
[GNU Arm Embedded Toolchain: 9-2019-q4-major](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads) is recommended.

See here to [setup the GNU ARM Embedded tools](https://docs.zephyrproject.org/2.3.0/getting_started/toolchain_3rd_party_x_compilers.html#gnu-arm-embedded)

If using Linux, v0.11.3 of the Zephyr SDK is recommended.

## Building the Firmware

See [here for build commands](https://github.com/LairdCP/Pinnacle_100_oob_demo/blob/master/docs/readme_ltem_aws.md#building-the-firmware).