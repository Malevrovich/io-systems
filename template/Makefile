ifneq ($(KERNELRELEASE),)
# kbuild part of makefile
obj-m  := template.o

ccflags-y := -I$(src)/..

else
# normal makefile
KDIR ?= /lib/modules/`uname -r`/build

all:
	$(MAKE) -C $(KDIR) M=$$PWD modules
 
clean:
	$(MAKE) -C $(KDIR) M=$$PWD clean

endif