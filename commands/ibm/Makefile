# Makefile for commands/ibm.

# See commands/simple/Makefile for a description.

CFLAGS	= -D_MINIX -D_POSIX_SOURCE
CCLD	= $(CC) -i $(CFLAGS)
MAKE	= exec make -$(MAKEFLAGS)
CC = exec cc

ALL	= \
	atnormalize \
	dosread \
	fdisk \
	format \
	loadfont \
	loadkeys \
	mixer \
	autopart \
	part \
	partition \
	playwave \
	postmort \
	recwave \
	repartition \
	screendump

all:	$(ALL)

dosread:	dosread.c
	$(CCLD) -o $@ $?
	install -S 16kw $@

atnormalize:	atnormalize.c
	$(CCLD) -o $@ $?
	install -S 16kw $@

fdisk:	fdisk.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

format:	format.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

loadfont:	loadfont.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

loadkeys:	loadkeys.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

mixer:	mixer.c
	$(CCLD) -o $@ $? -lcurses
	install -S 16kw $@

autopart:	autopart.c
	$(CCLD) -o $@ $?
	install -S 11kw $@

part:	part.c
	$(CCLD) -o $@ $?
	install -S 11kw $@

partition:	partition.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

playwave:	playwave.c
	$(CCLD) -o $@ $?
	install -S 16kw $@

postmort:	postmort.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

recwave:	recwave.c
	$(CCLD) -o $@ $?
	install -S 16kw $@

repartition:	repartition.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

screendump:	screendump.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

sdump:	sdump.c
	$(CCLD) -o $@ $?
	install -S 4kw $@

install:	\
	/usr/bin/atnormalize \
	/usr/bin/dosread \
		/usr/bin/dosdir \
		/usr/bin/doswrite \
	/usr/bin/fdisk \
	/usr/bin/format \
	/usr/bin/loadfont \
	/usr/bin/loadkeys \
	/usr/bin/mixer \
	/usr/bin/autopart \
	/usr/bin/part \
	/usr/bin/partition \
	/usr/bin/playwave \
	/usr/bin/postmort \
	/usr/bin/recwave \
	/usr/bin/repartition \
	/usr/bin/screendump \
	/bin/loadkeys \

/usr/bin/atnormalize:	atnormalize
	install -cs -o bin $? $@

/usr/bin/dosread:	dosread
	install -cs -o bin $? $@

/usr/bin/dosdir /usr/bin/doswrite:	/usr/bin/dosread
	install -l $? $@

/usr/bin/fdisk:	fdisk
	install -cs -o bin $? $@

/usr/bin/format:	format
	install -cs -o root -m 4755 $? $@

/usr/bin/loadfont:	loadfont
	install -cs -o bin $? $@

/usr/bin/loadkeys:	loadkeys
	install -cs -o bin $? $@

/usr/bin/mixer:	mixer
	install -cs -o bin $? $@

/usr/bin/autopart:	autopart
	install -lcs $? $@

/usr/bin/part:	part
	install -cs -o bin $? $@

/usr/bin/partition:	partition
	install -cs -o bin $? $@

/usr/bin/playwave:	playwave
	install -cs -o bin $? $@

/usr/bin/postmort:	postmort
	install -cs -o bin $? $@

/usr/bin/recwave:	recwave
	install -cs -o bin $? $@

/usr/bin/repartition:	repartition
	install -cs -o bin $? $@

/usr/bin/screendump:	screendump
	install -cs -o bin $? $@

/usr/bin/sdump:	sdump
	install -cs -o bin $? $@

/bin/loadkeys:	/usr/bin/loadkeys
	install -lcs $? $@

clean:
	rm -rf $(ALL) a.out core
