# auto generated makefile
HPT_ROOT := /home/dank/rr2640-linux-src-v1.3-legacy_single
HPT_REGPARM := $(shell echo "$(CFLAGS) $(KBUILD_CFLAGS)" | awk '{ match($$0,"-mregparm="); if (RSTART>0) print substr($$0,RSTART+10,1);}')
HPT_REGPARM := $(if $(HPT_REGPARM),$(HPT_REGPARM),0)
HPT_LIB := /home/dank/rr2640-linux-src-v1.3-legacy_single/lib/linux/free-x86_64-regparm$(HPT_REGPARM)
TARGETNAME := rr26xx
TARGETOBJS := os_linux.o osm_linux.o div64.o hptinfo.o config.o
TARGETMODS := him_odin.o ldm_raid_ls.o partition.o raid0.o raid1.o jbod.o raid5.o

obj-m := $(TARGETNAME).o

$(TARGETNAME)-objs := $(TARGETOBJS) $(TARGETMODS)

EXTRA_CFLAGS := -DLINUX -D_LINUX_ -D__KERNEL__=1 -DSUPPORT_ARRAY -DDBG=0 -DBITS_PER_LONG=64 -DMODVERSIONS -DMODULE -Idrivers/scsi -I$(HPT_ROOT)/inc/linux -I$(HPT_ROOT)/inc -I$(HPT_ROOT)/osm/linux

$(addprefix $(obj)/,$(TARGETOBJS:.o=.c)): FORCE
	@{ test -f /home/dank/rr2640-linux-src-v1.3-legacy_single/product/rr2640/linuxls/$(notdir $@) && cp -f /home/dank/rr2640-linux-src-v1.3-legacy_single/product/rr2640/linuxls/$(notdir $@) $@; } ||\
	{ test -f $(HPT_ROOT)/osm/linux/$(notdir $@) && cp -f $(HPT_ROOT)/osm/linux/$(notdir $@) $@; }

$(addprefix $(obj)/,$(TARGETMODS)): $(obj)/%.o: $(HPT_LIB)/%.o
	@cp -f $< $@
