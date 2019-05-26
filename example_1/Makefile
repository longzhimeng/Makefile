CC=gcc
obj=main.o print.o

#print the obj value
$(warning albert $(obj))

main: $(obj)
	@echo "albert:$(obj)"
	$(CC) -o main $(obj) 

$(obj): print.h
main.o: main.c 
	$(CC) -c main.c 
print.o: print.c
	$(CC) -c print.c 

.PHONY: clean 
clean:
	-rm -rf *.o main

