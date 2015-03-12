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
PKG_INSTALL_DIR:=$(1)/usr/

include $(INCLUDE_DIR)/package.mk

define Package/libctb
  SECTION:=administration
  CATEGORY:=Mnzn
  TITLE:=libctb
endef

define Build/Configure
endef

define Build/Compile
endef


$(eval $(call BuildPackage,libctb))
