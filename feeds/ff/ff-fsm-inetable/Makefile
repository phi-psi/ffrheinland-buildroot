#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#
# Package content copyright (C) 
# 2011      Katze Miau <miaukatzemiau@priveasy.de>
# 2012      egon_ffj <egon@freifunk-jena.de>
# 2012      Jan Huwald <jh@sotun.de>

include $(TOPDIR)/rules.mk

PKG_NAME:=ff-fsm-inetable
PKG_VERSION:=20120427
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ff-fsm-inetable
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:=Finite-state machine for Freifunk's node state
  DEPENDS:=+n2n +ff-hbbp
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ff-fsm-inetable/description
 Zustandsmaschine zur Einrichtung des Knotens zu Robinson/Drone/Queen/Ghost
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ff-fsm-inetable/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ff-fsm-inetable.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ff-fsm-inetable.postrm $(1)/CONTROL/postrm
endef

$(eval $(call BuildPackage,ff-fsm-inetable))
