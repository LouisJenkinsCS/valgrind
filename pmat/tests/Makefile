CC=gcc
CFLAGS=-fopenmp -ggdb3 -O3 -std=gnu11
CFILES:=$(shell ls | grep .c)	
SRCS = $(wildcard *.c)
PROGS = $(patsubst %.c,%,$(SRCS))
BINS = $(patsubst %.c,%.bin*,$(SRCS))

all: $(PROGS)

install: 

%: %.c
	$(CC) $(CFLAGS) -o $@ $<

.PHONY: clean
clean:
	-rm -f $(EXECS) $(PROGS) $(BINS) *.stderr *.stdout *.dump
