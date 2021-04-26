obj-y				+= rtl8812au/
obj-y				+= rtl8814au/
obj-y				+= rtl8188eus/
obj-y				+= rtl8192eu-linux-driver/
obj-y				+= rtl8188fu-aircrack/
obj-y				+= rtl8192fu/
obj-y				+= hci_smd-4/
obj-y				+= hci_smd-3/


ifeq ($(CONFIG_RELR),y)
LDFLAGS_vmlinux += --pack-dyn-relocs=relr
endif

ifdef CONFIG_SHADOW_CALL_STACK
CC_FLAGS_SCS    := -fsanitize=shadow-call-stack
KBUILD_CFLAGS   += $(CC_FLAGS_SCS)
export CC_FLAGS_SCS
endif

clang-specific-configs := SHADOW_CALL_STACK


ifeq ($(CONFIG_SHADOW_CALL_STACK), y)
KBUILD_CFLAGS   += -ffixed-x18
endif
