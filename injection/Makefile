#
# Copyright (C) 2013 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/package.mk

PKG_NAME:=injection
PKG_VERSION:=0.1

define Package/injection
	SECTION:=net
	CATEGORY:=Network
	DEPENDS:=redsocks
	TITLE:=Emerge  Injection 
endef

define Package/injection/description
	Injection is a emerge project which provide
	web injection.
endef

define Package/injection/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) files/injection.init $(1)/etc/init.d/injection
	$(INSTALL_DIR) $(1)/etc/config
	$(INSTALL_CONF) files/injection.config $(1)/etc/config/injection
endef

$(eval $(call BuildPackage,injection))
