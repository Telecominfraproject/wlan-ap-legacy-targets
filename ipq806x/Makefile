# Copyright (c) 2013 The Linux Foundation. All rights reserved.
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=ipq806x
BOARDNAME:=Qualcomm Atheros IPQ806X
FEATURES:=squashfs nand fpu ramdisk
CPU_TYPE:=cortex-a15
CPU_SUBTYPE:=neon-vfpv4
SUBTARGETS:=generic

KERNEL_PATCHVER:=5.4
KERNEL_TESTING_PATCHVER:=5.10

KERNELNAME:=zImage Image dtbs

GENERIC_BACKPORT_DIR := ${CURDIR}/backport-$(KERNEL_PATCHVER)
GENERIC_PATCH_DIR := ${CURDIR}/pending-$(KERNEL_PATCHVER)
GENERIC_HACK_DIR := ${CURDIR}/hack-$(KERNEL_PATCHVER)
GENERIC_FILES_DIR := ${CURDIR}/files-$(KERNEL_PATCHVER) 
GENERIC_LINUX_CONFIG:=${CURDIR}/config-$(KERNEL_PATCHVER)-generic

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += \
	kmod-leds-gpio kmod-gpio-button-hotplug swconfig \
	kmod-ata-ahci kmod-ata-ahci-platform \
	kmod-usb-ohci kmod-usb2 kmod-usb-ledtrig-usbport \
	kmod-phy-qcom-ipq806x-usb kmod-usb3 kmod-usb-dwc3-qcom \
	kmod-ath10k-ct wpad-basic-wolfssl \
	uboot-envtools

$(eval $(call BuildTarget))
