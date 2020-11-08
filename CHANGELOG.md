# Change Log
The version update instructions record each important update point for everyone to track and understand.

## Release Notes
- Date: Version update date.
- Importance: The difference between five stars, the more stars the more important.
- Types: ADD / UPDATE / TOOL / BUG
- description: Detailed description of the update.
- Path: Link to related files.
- Firmware: Targeted OpenWrt firmware.

| Date | Firmware | Types | Importance | Path | description |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 2020.11.08 | Phicomm-N1, S905x3-Boxs | TOOL | ✩✩✩ | [dtb-amlogic](https://github.com/ophub/op/tree/main/router/phicomm_n1/armbian/dtb-amlogic) | The dtb library is added to facilitate the lack of corresponding boot files when compiling the firmware of related models with the old version of the kernel file. |
| - | Phicomm-N1, S905x3-Boxs | TOOL | ✩✩✩ | [update_dtb.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/build_kernel/update_dtb.sh) | Update kernel.tar.xz files in the kernel directory with the latest dtb file. |
| - | Phicomm-N1, S905x3-Boxs | UPDATE | ✩✩✩ | [kernel](https://github.com/ophub/op/tree/main/router/phicomm_n1/armbian/phicomm-n1/kernel) | Supplement the old version of the kernel with the latest dtb file. |
| - | Phicomm-N1, S905x3-Boxs | UPDATE | ✩✩ | [make_use_img.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/build_kernel/make_use_img.sh) | When the kernel is extracted, if the file lacks a key .dtb file, the supplement will be extracted from the dtb library. |
| - | Phicomm-N1, S905x3-Boxs | UPDATE | ✩✩ | [make_use_kernel.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/build_kernel/make_use_kernel.sh) | When the kernel is extracted, if the file lacks a key .dtb file, the supplement will be extracted from the dtb library. |
| - | Phicomm-N1, S905x3-Boxs | UPDATE | ✩✩ | [s905x3-install.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/install-program/files/s905x3-install.sh) | Added that if the dtb file is missing during installation, the download path will be prompted. |
| 2020.11.07 | Phicomm-N1, S905x3-Boxs | ADD | ✩✩ | [5.4.75](https://github.com/ophub/op/tree/main/router/phicomm_n1/armbian/phicomm-n1/kernel/5.4.75) | Add New kernel. |
| - | Phicomm-N1, S905x3-Boxs | ADD | ✩✩ | [5.9.5](https://github.com/ophub/op/tree/main/router/phicomm_n1/armbian/phicomm-n1/kernel/5.9.5) | Add New kernel. |
| - | Phicomm-N1, S905x3-Boxs | UPDATE | ✩✩ | [make_use_img.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/build_kernel/make_use_img.sh) | Add fuzzy matching function. When the version specified by the script is not found, other firmware will be searched from the flippy directory. Thus, you can directly put the kernel file you want to use into the flippy directory for extraction, without manually changing the relevant parameters each time. |
| - | Phicomm-N1, S905x3-Boxs | UPDATE | ✩✩ | [make_use_kernel.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/build_kernel/make_use_kernel.sh) | Add fuzzy matching function. When the version specified by the script is not found, other firmware will be searched from the flippy directory. Thus, you can directly put the kernel file you want to use into the flippy directory for extraction, without manually changing the relevant parameters each time. |
| 2020.11.05 | S905x3-Boxs | UPDATE | ✩✩ | [build-openwrt-s905x3.yml](https://github.com/ophub/op/blob/main/.github/workflows/build-openwrt-s905x3.yml) | Use the environment variable GITHUB_REPOSITORY to replace ophub/op, so that fork users can call their own compiled phicomm-n1 firmware to compile the s905x3-boxs series firmware instead of pointing to the releases of this warehouse. |
| - | Phicomm-N1 | UPDATE | ✩✩ | [test-build-phicomm_n1.yml](https://github.com/ophub/op/blob/main/.github/workflows/test-build-phicomm_n1.yml) | Use the environment variable GITHUB_REPOSITORY to replace ophub/op, so that fork users can call their own compiled phicomm-n1 firmware to compile the new version of the firmware instead of pointing to the releases in this warehouse. |
| 2020.11.03 | All firmware | UPDATE | ✩✩ | [.config](https://github.com/ophub/op/blob/main/router/x64/.config) | Several software packages such as lsblk are integrated by default when the firmware is compiled, which supports later use in firmware maintenance. |
| 2020.11.01 | Phicomm-N1, S905x3-Boxs | ADD | ✩✩ | [s905x3-install.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/install-program/files/s905x3-install.sh) | Added the function of writing emmc partition to s905x3 series boxes. |
| - | Phicomm-N1, S905x3-Boxs | ADD | ✩✩ | [s905x3-update.sh](https://github.com/ophub/op/blob/main/router/phicomm_n1/install-program/files/s905x3-update.sh) | Added the function of updating emmc partition firmware to s905x3 series boxes. |


