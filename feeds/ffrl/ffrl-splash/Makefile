#
# Copyright (C) 2006-2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

# Package content copyright (C) 
# 2011-2012 Jan Huwald <jh@sotun.de>
#      2012 Freifunk Rheinland e. V. <http://www.freifunk-rheinland.net/>


include $(TOPDIR)/rules.mk

PKG_NAME:=ffrl-splash
PKG_VERSION:=20120624
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-splash
  SECTION:=base
  CATEGORY:=Utilities
  SUBMENU:=Freifunk Rheinland
  PKGARCH:=all
  DEFAULT:=n
  TITLE:=Freifunk web-splash
# MAINTAINER:=
  URL:=https://freifunk-rheinland.net/wiki/index.php/Firmwarebeschreibung
  DEPENDS:=+ffrl-fsm-inetable
endef

define Package/ffrl-splash/description
  Splash screen for Freifunk users
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-splash/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ffrl-splash.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ffrl-splash.postrm $(1)/CONTROL/postrm
endef

$(eval $(call BuildPackage,ffrl-splash))
