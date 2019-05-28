#get cacu bin file
cc  = gcc
VPATH =	src include
INCLUDES = -I include
COMPILE.C = $(cc) $(INCLUDES) -c $<  -ggdb

TARGET = cacu

SRCS = \
	add_int.c \
	add_float.c \
	sub_int.c \
	sub_float.c \
	main.c 

OBJS = $(addsuffix .o, $(basename $(SRCS)))

$(TARGET): $(OBJS)
	$(cc) $^ -o $@ -ggdb

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

#clean project
.PHONY: clean
clean:
	rm -f $(TARGET) $(OBJS)
