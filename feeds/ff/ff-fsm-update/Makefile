#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#
# Package content copyright (C) 
# 2011      Katze Miau <miaukatzemiau@priveasy.de>

include $(TOPDIR)/rules.mk

PKG_NAME:=ff-fsm-update
PKG_VERSION:=20111206
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ff-fsm-update
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:=Finite-state machine for Freifunk update tasks
  DEPENDS:=+ff-fsm-inetable +ff-hbbp
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ff-fsm-update/description
 Zustandsmaschine für Knotenupdates
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ff-fsm-update/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ff-fsm-update.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ff-fsm-update.postrm $(1)/CONTROL/postrm
endef

$(eval $(call BuildPackage,ff-fsm-update))
