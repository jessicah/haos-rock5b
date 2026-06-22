# Home Assistant Operating System for ROCK5B

This is a build of HAOS for the ROCK5B, where I have merged the HAOS buildroot with
the upstream buildroot at tag 2026.05, and added additional supporting configuration
for the ROCK5B platform, utilising the Linux and U-Boot trees provided by Collabora.

## Modifying U-Boot for SPI Flash

HAOS also requires a modified `u-boot` for the SPI flash, as HAOS includes a patch to
`u-boot` that affects how booting works.

Requirements:

1. https://gitlab.collabora.com/hardware-enablement/rockchip-3588/u-boot/-/archive/v2026.01/u-boot-v2026.01.tar.gz
2. https://github.com/jessicah/haos-rock5b/blob/rock5b/buildroot-external/patches/uboot/0001-CMD-read-string-from-fileinto-env.patch

After patching, the rest of the instructions at https://gitlab.collabora.com/hardware-enablement/rockchip-3588/notes-for-rockchip-3588/-/blob/main/upstream_uboot.md
should be followed.

## HAOS ROCK5B Repositories

- https://github.com/jessicah/haos-rock5b/tree/rock5b
- https://github.com/jessicah/buildroot/tree/haos-onto-upstream-2026.05

## References

- https://gitlab.collabora.com/hardware-enablement/rockchip-3588/linux
- https://gitlab.collabora.com/hardware-enablement/rockchip-3588/u-boot
- https://gitlab.com/buildroot.org/buildroot/
- https://github.com/home-assistant/operating-system
- https://github.com/home-assistant/buildroot
