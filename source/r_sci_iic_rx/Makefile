MODULE_NAME = 	r_sci_iic_rx
VERSION = 		v2.45

CONFIG_FOLDER = r_config
TARGET_FOLDER = ../../FITModules

$(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).zip: $(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).xml $(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).mdf $(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION)_extend.mdf
	cd ./$(MODULE_NAME)_vx.xx; \
	mkdir $(CONFIG_FOLDER); \
	cp $(MODULE_NAME)/ref/$(MODULE_NAME)_config_reference.h $(CONFIG_FOLDER)/$(MODULE_NAME)_config.h; \
	cp $(MODULE_NAME)/ref/$(MODULE_NAME)_pin_config_reference.h $(CONFIG_FOLDER)/$(MODULE_NAME)_pin_config.h; \
	zip ../$(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).zip -r ./$(MODULE_NAME) -r ./$(CONFIG_FOLDER); \
	rm -rf $(CONFIG_FOLDER); \
	cd ../;	\

$(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).xml:
	cp ./$(MODULE_NAME)_vx.xx.xml $(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).xml

$(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).mdf:
	cp ./$(MODULE_NAME)_vx.xx.mdf $(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION).mdf

$(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION)_extend.mdf:
	cp ./$(MODULE_NAME)_vx.xx_extend.mdf $(TARGET_FOLDER)/$(MODULE_NAME)_$(VERSION)_extend.mdf

clean:
	rm -rf $(TARGET_FOLDER)/$(MODULE_NAME)*.*
