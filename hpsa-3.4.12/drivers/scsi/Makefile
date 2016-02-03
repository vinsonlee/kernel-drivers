obj-m := hpsa.o

ifeq (${KVER},)
	KVER := $(shell echo `uname -r`)
endif

KDIR  := /lib/modules/$(KVER)/build
PWD   := $(shell pwd)

default:
	$(MAKE) -C $(KDIR) M=$(PWD) modules

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean

install:
	$(MAKE) -C $(KDIR) M=$(PWD) modules_install

