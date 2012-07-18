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

PKG_NAME:=ffrl-fsm-inetable
PKG_VERSION:=20120718
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-fsm-inetable
  SECTION:=base
  CATEGORY:=Utilities
  SUBMENU:=Freifunk Rheinland
  PKGARCH:=all
  DEFAULT:=n
  TITLE:=Finite-state machine for network states
# MAINTAINER:=
  URL:=https://freifunk-rheinland.net/wiki/index.php/Firmwarebeschreibung
  DEPENDS:=+ffrl-fsm
endef

define Package/ffrl-fsm-inetable/description
  Controls the different network states that result of the local
  availability of internet connection and the state of the cloud. 
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-fsm-inetable/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ff-fsm-inetable.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ff-fsm-inetable.postrm $(1)/CONTROL/postrm
#	$(INSTALL_DIR) $(1)/usr/sbin
#	$(INSTALL_BIN) $(PKG_BUILD_DIR)/fsm $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,ffrl-fsm-inetable))
