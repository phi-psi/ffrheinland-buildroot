#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#
# Package content copyright (C) 
# 2011      Katze Miau <miaukatzemiau@priveasy.de>
# 2012      Jan Huwald <jh@sotun.de>

include $(TOPDIR)/rules.mk

PKG_NAME:=ff-splash
PKG_VERSION:=20120427
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ff-splash
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:=Freifunk's splash pages
  DEPENDS:=+ff-fsm-inetable +ff-hbbp
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ff-splash/description
  Splash screen for Freifunk users
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ff-splash/install
	$(CP) -ap files/root/* $(1)/
	mkdir -p $(1)/CONTROL
	$(INSTALL_BIN) ./ipkg/ff-splash.postinst $(1)/CONTROL/postinst
	$(INSTALL_BIN) ./ipkg/ff-splash.postrm $(1)/CONTROL/postrm
endef

$(eval $(call BuildPackage,ff-splash))
