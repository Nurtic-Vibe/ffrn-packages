include $(TOPDIR)/rules.mk

PKG_NAME:=ffrn-lowmem-patches
PKG_VERSION:=1

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/ffrn-lowmem-patches
  SECTION:=gluon
  CATEGORY:=Gluon
  TITLE:=Patch files for routers with only 32mb ram
  DEPENDS:=+gluon-core
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffrn-lowmem-patches/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/etc/init.d/ffrn-lowmem $(1)/etc/init.d/ffrn-lowmem
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) ./files/usr/sbin/ffrn-lowmem $(1)/usr/sbin/ffrn-lowmem
endef

$(eval $(call BuildPackage,ffrn-lowmem-patches))
