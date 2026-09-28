ASM nasm

SRC_DIR src
BUILD_DIR build

$(BUILD_DIR)/StartFloppy.img: $(BUILD_DIR)/Start.bin
	cp $(BUILD_DIR)/Start.bin $(BUILD_DIR)/StartFloppy.img
	truncate -s 1440k $(BUILD_DIR)/StartFloppy.img

$(BUILD_DIR)/Start.bin: $(SRC_DIR)/asm/Start.S
	$(ASM) $(SRC_DIR)/asm/Start.S -f bin -o $(BUILD_DIR)/Start.bin
