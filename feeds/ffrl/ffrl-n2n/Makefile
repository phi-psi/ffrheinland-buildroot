#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#

include $(TOPDIR)/rules.mk


PKG_NAME:=ffrl-n2n
PKG_VERSION:=0.0.3875.20120414
PKG_RELEASE:=1
#PKG_REV:=

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_BUILD_DEPENDS := uci base-files

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-n2n
  SECTION:=ffrl
  CATEGORY:=Network
  TITLE:=Freifunk Rheinland - n2n init script
  DEPENDS:=+base-files +n2n
  URL:=http://www.freifunk-rheinland.net
  DEFAULT:=n
  PKGARCH:=all
endef

define Package/ffrl-n2n/description
 Ein Initialisierungsskript, welches den Router mit anderen Routern in der
 gleichen Freifunkzelle über n2n-VPN verbindet.
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrl-n2n/install
	$(CP) -ap files/root/* $(1)/
endef

$(eval $(call BuildPackage,ffrl-n2n))
