include $(TOPDIR)/rules.mk

PKG_NAME:=fastfetch
PKG_VERSION:=2.35.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/fastfetch-cli/fastfetch/archive/refs/tags/
PKG_HASH:=e066d84f9ca176e24f162ce99dab7fac5238b5e8c94ab4aaff5850b6cc5c6ead

PKG_BUILD_DIR:=$(BUILD_DIR)/fastfetch-$(PKG_VERSION)

PKG_MAINTAINER:=
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/fastfetch
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Fetch and display system information
endef

define Package/fastfetch/description
  A maintained, feature-rich and performance oriented, neofetch like system information tool.
endef

define Package/fastfetch/install
    $(INSTALL_DIR) $(1)/usr/bin
    $(INSTALL_BIN) $(PKG_BUILD_DIR)/fastfetch $(1)/usr/bin/
endef

$(eval $(call BuildPackage,fastfetch))
