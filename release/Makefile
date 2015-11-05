WIN32_DIR	= xtensa-toolchain
OSX_DIR = xtensa-toolchain
LINUX32_DIR = xtensa-toolchain
LINUX64_DIR = xtensa-toolchain

WIN32_TC = $(addprefix $(WIN32_DIR),-mk-win32.zip)
OSX_TC = $(addprefix $(OSX_DIR),-mk-osx.tar.xz)
LINUX32_TC = $(addprefix $(LINUX32_DIR),-mk-linux32.tar.xz)
LINUX64_TC = $(addprefix $(LINUX64_DIR),-mk-linux64.tar.xz)

all: win32 osx linux32 linux64

clean:
	rm -rf $(WIN32_DIR)
	rm -rf $(OSX_DIR)
	rm -rf $(LINUX32_DIR)
	rm -rf $(LINUX64_DIR)

win32:
	@echo "Generating the Xtensa Toolchain of Win32"
	rm -rf $(WIN32_DIR)
	mkdir -p $(WIN32_DIR)/bin
	cp ../espota.py $(WIN32_DIR)/bin
	cp -R ../doc $(WIN32_DIR)
	unzip -ju -d $(WIN32_DIR)/bin ../dist/esptool-*-win*.zip
	unzip -ju -d $(WIN32_DIR)/bin ../dist/mkspiffs-*-win*.zip
	tar zxf ../dist/win32-xtensa-*.tar.gz -C $(WIN32_DIR)
	zip -9r $(WIN32_TC) $(WIN32_DIR)

osx:
	@echo "Generating the Xtensa Toolchain of OSX"
	rm -rf $(OSX_DIR)
	mkdir -p $(OSX_DIR)/bin
	cp ../espota.py $(OSX_DIR)/bin
	cp -R ../doc $(OSX_DIR)
	tar zxf ../dist/esptool-*-osx*.tar.gz -C $(OSX_DIR)/bin --strip-components=1 
	tar zxf ../dist/mkspiffs-*-osx*.tar.gz -C $(OSX_DIR)/bin --strip-components=1 
	tar zxf ../dist/osx-xtensa-*.tar.gz -C $(OSX_DIR)
	tar cJf $(OSX_TC) $(OSX_DIR)

linux32:
	@echo "Generating the Xtensa Toolchain of Linux32"
	rm -rf $(LINUX32_DIR)
	mkdir -p $(LINUX32_DIR)/bin
	cp ../espota.py $(LINUX32_DIR)/bin
	cp -R ../doc $(LINUX32_DIR)
	tar zxf ../dist/esptool-*-linux32*.tar.gz -C $(LINUX32_DIR)/bin --strip-components=1 
	tar zxf ../dist/mkspiffs-*-linux32*.tar.gz -C $(LINUX32_DIR)/bin --strip-components=1 
	tar zxf ../dist/linux32-xtensa-*.tar.gz -C $(LINUX32_DIR)
	tar cJf $(LINUX32_TC) $(LINUX32_DIR)

linux64:
	@echo "Generating the Xtensa Toolchain of Linux64"
	rm -rf $(LINUX64_DIR)
	mkdir -p $(LINUX64_DIR)/bin
	cp ../espota.py $(LINUX64_DIR)/bin
	cp -R ../doc $(LINUX64_DIR)
	tar zxf ../dist/esptool-*-linux64*.tar.gz -C $(LINUX64_DIR)/bin --strip-components=1 
	tar zxf ../dist/mkspiffs-*-linux64*.tar.gz -C $(LINUX64_DIR)/bin --strip-components=1 
	tar zxf ../dist/linux64-xtensa-*.tar.gz -C $(LINUX64_DIR)
	tar cJf $(LINUX64_TC) $(LINUX64_DIR)
