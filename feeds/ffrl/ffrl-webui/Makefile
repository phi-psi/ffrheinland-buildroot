#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ffrl-webui
PKG_VERSION:=0.0.20120509
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-webui
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:=Web user interface for FFM
  DEPENDS:=+base-files +uhttpd
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ffrl-webui/description
 Der Kern und die Magie eines Freifunk-Rheinland-Knotens
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-webui/install
	$(CP) -ap files/root/* $(1)/
endef

$(eval $(call BuildPackage,ffrl-webui))
