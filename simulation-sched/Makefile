CC=gcc

.PHONY: all clean

PRJ_BINS=sched_dummy
PRJ_OBJS=$(addsuffix .o,$(PRJ_BINS))

all: $(PRJ_BINS)

$(PRJ_BINS): $(PRJ_OBJS)

%: %.o
	$(CC) -D_MACHTYPE_LINUX $< -o $@

%.o: %.c
	$(CC) -D_MACHTYPE_LINUX $< -c -o $@

clean:
	@echo "Cleaning up..."
	rm -f *.o
	rm -f $(PRJ_BINS)
