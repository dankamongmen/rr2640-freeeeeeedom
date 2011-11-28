# $Id: Makefile,v 1.3 2009/09/25 01:34:48 wsw Exp $
#
# Copyright (C) 2010 HighPoint Technologies, Inc.
# All Rights Reserved.
#

HPT_ROOT := ../../..

C_DEFINES := -DSUPPORT_ARRAY

TARGETNAME := rr26xx
TARGETTYPE := KMOD
TARGETMODS := him_odin.o ldm_raid_ls.o partition.o raid0.o raid1.o jbod.o raid5.o
TARGETOBJS := os_linux.o osm_linux.o div64.o hptinfo.o config.o

# files to delete when make clean
TRASH:=./update_revision.sh ./spp

include $(HPT_ROOT)/inc/linux/Makefile.def

$(TARGETOBJS): osm_linux.h
