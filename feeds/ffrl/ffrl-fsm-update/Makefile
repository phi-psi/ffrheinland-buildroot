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

PKG_NAME:=ffrl-fsm-update
PKG_VERSION:=20111206
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-fsm-update
  SECTION:=base
  CATEGORY:=Utilities
  SUBMENU:=Freifunk Rheinland
  PKGARCH:=all
  DEFAULT:=n
  TITLE:=Finite-state machine for node update tasks
# MAINTAINER:=
  URL:=https://freifunk-rheinland.net/wiki/index.php/Firmwarebeschreibung
  DEPENDS:=+ffrl-fsm
endef

define Package/ffrl-fsm-update/description
  Implements all-or-nothing update of nodes.
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-fsm-update/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ff-fsm-update.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ff-fsm-update.postrm $(1)/CONTROL/postrm
#	$(INSTALL_DIR) $(1)/usr/sbin
#	$(INSTALL_BIN) $(PKG_BUILD_DIR)/fsm $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,ffrl-fsm-update))
