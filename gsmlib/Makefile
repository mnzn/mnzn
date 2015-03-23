include $(TOPDIR)/rules.mk

PKG_NAME:=gsmlib
PKG_VERSION:=master
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=https://github.com/mnzn/gsmlib.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=master
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_INSTALL:=1
#PKG_BUILD_DEPENDS:=libpthread libstdcpp

CXX="$(TARGET_CROSS)g++"
RANLIB="$(TARGET_CROSS)ranlib"
AR="$(TARGET_CROSS)ar"

include $(INCLUDE_DIR)/package.mk

define Package/gsmlib
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=gsmlib,another lib for gsmopen
#  DEPENDS:=+libstdcpp +libpthread
endef

define Package/gsmlib/description
    The lib for gsmopen
endef

define Build/Configure
	$(call Build/Configure/Default,--prefix=/usr)
endef

define Build/Compile
#	CROSS="true" \
#	CFLAGS="$(TARGET_CFLAGS)" \
#	CXXFLAGS="$(TARGET_CFLAGS)" \
#	CXX="$(TARGET_CROSS)g++" \
#	ARCH="$(ARCH)" \
#	LDFLAGS="$(TARGET_LDFLAGS)" \
#	RANLIB="$(TARGET_CROSS)ranlib" \
#	AR="$(TARGET_CROSS)ar" \
	$(call Build/Compile/Default)
endef

define Build/Install
    $(call Build/Install/Default,install)
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/include $(1)/usr
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libgsm*.{a,so*} $(1)/usr/lib/
endef


define Package/gsmlib/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libgsm* $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include $(1)/usr

endef


$(eval $(call BuildPackage,gsmlib))
