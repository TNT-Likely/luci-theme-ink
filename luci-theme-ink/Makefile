#
# Ink theme for LuCI — PanWatch-inspired (indigo / deep-navy)
# Based on luci-theme-bootstrap.
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

LUCI_TITLE:=Ink Theme (PanWatch-inspired, light/dark)
LUCI_DEPENDS:=+luci-base

PKG_VERSION:=0.1.0
PKG_RELEASE:=1

PKG_LICENSE:=Apache-2.0
PKG_MAINTAINER:=TNT-Likely

define Package/luci-theme-ink/postrm
#!/bin/sh
[ -n "$${IPKG_INSTROOT}" ] || {
	uci -q delete luci.themes.Ink
	uci commit luci
}
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
