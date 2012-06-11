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

PKG_NAME:=ff-hbbp
PKG_VERSION:=20120427
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ff-hbbp
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:= Home-Based Broadcast Protocol - Freifunk TX/RX
  DEPENDS:=+hbbp
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ff-hbbp/description
  Home-Based Broadcast Protocol Sender und Empfänger für Freifunk Knoten
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ff-hbbp/install
	$(CP) -ap files/root/* $(1)/
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/hbbp.init $(1)/etc/init.d/hbbp
endef

$(eval $(call BuildPackage,ff-hbbp))
