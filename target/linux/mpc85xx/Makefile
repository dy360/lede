#
# Copyright (C) 2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=powerpc
BOARD:=mpc85xx
BOARDNAME:=Freescale MPC85xx
CPU_TYPE:=8540
FEATURES:=squashfs
MAINTAINER:=Imre Kaloz <kaloz@openwrt.org>
SUBTARGETS:=generic p1020

KERNEL_PATCHVER:=4.9

define Target/Description
	Build images for the Freescale MPC85xx based boards.
endef

include $(INCLUDE_DIR)/target.mk

KERNEL_IMAGES := zImage
ifeq ($(SUBTARGET),generic)
KERNEL_IMAGES += cuImage.tl-wdr4900-v1
endif

DEFAULT_PACKAGES += \
	kmod-input-core kmod-input-gpio-keys kmod-button-hotplug \
	kmod-leds-gpio swconfig kmod-ath9k wpad-mini

$(eval $(call BuildTarget))
