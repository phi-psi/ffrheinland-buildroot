#
# Copyright (C) 2006-2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

# Package content copyright (C) 
#      2012 Freifunk Rheinland e. V. <http://www.freifunk-rheinland.net/>


include $(TOPDIR)/rules.mk

PKG_NAME:=ffrl-n2n-watchdog
PKG_VERSION:=20120718
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-n2n-watchdog
  SECTION:=base
  CATEGORY:=Utilities
  SUBMENU:=Freifunk Rheinland
  PKGARCH:=all
  DEFAULT:=n
  TITLE:=restarts n2n if needed
# MAINTAINER:=
  URL:=https://freifunk-rheinland.net/wiki/index.php/Firmwarebeschreibung
  DEPENDS:=+ffrl-fsm
endef

define Package/ffrl-n2n-watchdog/description
  Wacht über die n2n-Verbindungen und startet sie gegebenfalls neu.
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-n2n-watchdog/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ff-fsm-inetable.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ff-fsm-inetable.postrm $(1)/CONTROL/postrm
endef

$(eval $(call BuildPackage,ffrl-n2n-watchdog))
