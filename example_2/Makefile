#get cacu bin file
cc  = gcc
VPATH =	src include
CPPFLAGS = -I include
obj = add_int.o add_float.o sub_int.o sub_float.o main.o

cacu: $(obj)
	$(cc) $^ -o $@ -ggdb

#get add_int.o target
add_int.o: add_int.c add.h
	$(cc) $(CPPFLAGS) -c $<  -ggdb

#get add_float.o target
add_float.o: add_float.c add.h
	$(cc) $(CPPFLAGS) -c $<  -ggdb

#get sub_int.o target
sub_int.o: sub_int.c sub.h
	$(cc) $(CPPFLAGS) -c $<  -ggdb

#get sub_float.o target
sub_float.o: sub_float.c sub.h
	$(cc) $(CPPFLAGS) -c $<  -ggdb

#get main.o target
main.o:main.c add.h sub.h
	$(cc) $(CPPFLAGS) -c $<  -ggdb

#clean project
clean:
	rm -f cacu *.o
