#
# Copyright (C) 2011-2015 Entware
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

all: .done

.done:
	patch -d $(TOP) -p3 -i $(CURDIR)/fix-path.patch
	rm -f ../../../openwrt_trunk/feeds/oldpackages/multimedia/ushare/files/ushare.*
	cp -f ./555-flv-support.patch ../../../openwrt_trunk/feeds/oldpackages/multimedia/ushare/patches/
	cp -f ./S99ushare ../../../openwrt_trunk/feeds/oldpackages/multimedia/ushare/files/
	@touch $@

clean:
	@rm -f .done

.PHONY: clean
