# cmvision

## cmvision port for ROS Noetic. Tested on Ubuntu 20.04

### Dependancies

* WxWidgets

    ```sh
    apt install --no-install-recommends -y \
    libgtk-3-dev  \
    wx3.0-headers \
    libwxgtk3.0-gtk3-dev
    ```
### Usage

1. Use `colorgui` node to select the color ranges for your blobs (Sample launch file in `launch/colorgui.launch`)

    * Click on the colors you want as the images play on the window. The **AB** range will get updated with the each click. 
      Use this range in the colors file (Sample file in `config/colors.txt`)

2. Use `cmvision` node for blob detection (Sample launch file in `launch/cmvision.launch`)

    * Pass the colors file with param `cmvision/color_file`

    * Set param `cmvision/debug_on` to `true` to display the detections
