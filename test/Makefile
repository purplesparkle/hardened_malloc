CONFIG_SLAB_CANARY := true
CONFIG_EXTENDED_SIZE_CLASSES := true

ifeq (,$(filter $(CONFIG_SLAB_CANARY),true false))
    $(error CONFIG_SLAB_CANARY must be true or false)
endif

LDLIBS := -lpthread

CPPFLAGS += \
    -DSLAB_CANARY=$(CONFIG_SLAB_CANARY) \
    -DCONFIG_EXTENDED_SIZE_CLASSES=$(CONFIG_EXTENDED_SIZE_CLASSES)

EXECUTABLES := \
    offset \
    mallinfo \
    malloc_info \
    large_array_growth

all: $(EXECUTABLES)

clean:
	rm -f $(EXECUTABLES)
