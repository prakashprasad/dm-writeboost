KERNEL_TREE := /lib/modules/$(shell uname -r)/build
# KERNEL_TREE := $(HOME)/linux-$(KERN_VERSION)

PWD := $(shell pwd)

# EXTRA_CFLAGS += -O0 -DCONFIG_DM_DEBUG -fno-inline -Wall
# EXTRA_CFLAGS += -O2 -UCONFIG_DM_DEBUG

obj-m := dm-writeboost.o
dm-writeboost-objs := \
	dm-writeboost-target.o \
	dm-writeboost-metadata.o \
	dm-writeboost-daemon.o

all:
	$(MAKE) -C $(KERNEL_TREE) M=$(PWD) modules

clean:
	$(MAKE) -C $(KERNEL_TREE) M=$(PWD) clean
