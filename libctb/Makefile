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
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=libctb,a lib for gsmopen
endef

define Package/libctb/description
    The lib for gsmopen
endef

define Build/Compile
    (cd $(PKG_BUILD_DIR)/build/)
    $(call Build/Compile/Default) 
endef


#define Build/InstallDev
#    $(INSTALL_DIR) $(1)/usr/include
#    $(INSTALL_DIR) $(1)/usr/lib
#    $(CP) $(PKG_INSTALL_DIR)/usr/include $(1)/usr
#    $(CP) $(PKG_INSTALL_DIR)/usr/lib/lib$(PKG_NAME).{a,so*} $(1)/usr/lib/
#endef
#
#
#define Package/libhttp-parser/install
#    $(INSTALL_DIR) $(1)/usr/lib
#    $(CP) $(PKG_BUILD_DIR)/libhttp_parser.so.* $(1)/usr/lib/
#    ( cd $(1)/usr/lib ; ln -s libhttp_parser.so.* libhttp_parser.so )
#endef

define Build/Configure
endef

define Build/Compile
endef


$(eval $(call BuildPackage,libctb))
