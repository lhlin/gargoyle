#
# Copyright (C) 2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=usb-modeswitch-data
PKG_VERSION:=20130610
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=http://www.draisberghof.de/usb_modeswitch/
PKG_MD5SUM:=52dff3f54e0c01dad02639d642e089e0

include $(INCLUDE_DIR)/package.mk

define Package/usb-modeswitch-data
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=usb-modeswitch
  TITLE:=USB ModeSwitch - Dongle configuration database
  URL:=http://packages.debian.org/de/sid/usb-modeswitch-data
endef

define Package/usb-modeswitch-data/description
  Configuration database for usb-modeswitch.
  Contains definitions for many USB devices required to
  autoswitch "flip flop" gear.
endef

define Build/Compile
endef

define Package/usb-modeswitch-data/install
	$(INSTALL_DIR) $(1)/etc/usb_modeswitch.d/
	$(CP) $(PKG_BUILD_DIR)/usb_modeswitch.d/* $(1)/etc/usb_modeswitch.d/
endef

$(eval $(call BuildPackage,usb-modeswitch-data))
