#
# Copyright (C) 2012 Freifunk Rheinland
#
# This is free software, licensed under the GNU General Public License v3.
# See http://www.gnu.org/licenses/ for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ffrl-fsm
PKG_VERSION:=0.0.20120509
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/ffrl-fsm
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Freifunk Rheinland
  TITLE:=Finite-state machine for Freifunk Rheinland
  DEPENDS:=+base-files +kmod-batman-adv +flock +n2n +udp-broadcast +radvd \
	+wide-dhcpv6-server +iptables-mod-conntrack-extra \
	+iptables-mod-conntrack-extra +iptables-mod-filter +iptables-mod-ipp2p \
	+iptables-mod-nat-extra	+ip6tables iperf-mt +l7-protocols +ffrl-webui
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
