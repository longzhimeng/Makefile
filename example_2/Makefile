#get cacu bin file
CC  = gcc
VPATH =	src include
CPPFLAGS = -I include
COMPILE.C = $(CC) $(CPPFLAGS) -c $<  -ggdb

TARGET = cacu

SRCS = \
	add_int.c \
	add_float.c \
	sub_int.c \
	sub_float.c \
	main.c 

OBJS = $(addsuffix .o, $(basename $(SRCS)))

$(TARGET): $(OBJS)
	$(CC) $^ -o $@ -ggdb

#get add_int.o target
add_int.o: add_int.c add.h
	$(COMPILE.C)

#get add_float.o target
add_float.o: add_float.c add.h
	$(COMPILE.C)

#get sub_int.o target
sub_int.o: sub_int.c sub.h
	$(COMPILE.C)

#get sub_float.o target
sub_float.o: sub_float.c sub.h
	$(COMPILE.C)

#get main.o target
main.o:main.c add.h sub.h
	$(COMPILE.C)

#----------automatic dependency generaton beging -------------
include $(subst .c,.d,$(SRCS))

%.d: %.c
	$(CC) -M $(CPPFLAGS) $< > $@.$$$$; \
	sed 's,\($*\)\.o[ :]*,\1.o $@ : ,g' < $@.$$$$ > $@; \
	$(RM) $@.$$$$
#----------automatic dependency generaton end -------------


#clean project
.PHONY: clean
clean:
	$(RM) $(TARGET) $(OBJS) *.d
