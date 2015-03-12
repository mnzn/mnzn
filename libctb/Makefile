include $(TOPDIR)/rules.mk

PKG_NAME:=libctb
PKG_VERSION:=master
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=https://github.com/mnzn/libctb.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=master
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/libctb
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=libctb,a lib for gsmopen
endef

define Package/libctb/description
    The lib for gsmopen
endef

define Build/Compile
    $(MAKE) -C $(PKG_BUILD_DIR)/build -f ./GNUmakefile
endef

#define Build/Install
#	$(MAKE) -C $(PKG_BUILD_DIR)/build -f ./GNUmakefile install
#endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/include $(1)/usr
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/lib$(PKG_NAME).{a,so*} $(1)/usr/lib/
endef


define Package/libctb/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/lib/libctb-0.16.a $(1)/usr/lib/
	$(CP) $(PKG_BUILD_DIR)/lib/libctb-0.16.so $(1)/usr/lib/
endef


$(eval $(call BuildPackage,libctb))
