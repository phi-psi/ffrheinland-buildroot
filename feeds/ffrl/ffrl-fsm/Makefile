#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#

include $(TOPDIR)/rules.mk


PKG_NAME:=ffrl-fsm
PKG_VERSION:=0.0.20120404
PKG_RELEASE:=1
#PKG_REV:=

#PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
#PKG_BUILD_DEPENDS := uci base-files

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-fsm
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:=Finite-state machine for Freifunk Rheinland
  DEPENDS:=+base-files +ffrl-miniconfig
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ffrl-fsm/description
 Der Kern und die Magie eines Freifunk-Rheinland-Knotens
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-fsm/install
	$(CP) -ap files/root/* $(1)/
endef

$(eval $(call BuildPackage,ffrl-fsm))
