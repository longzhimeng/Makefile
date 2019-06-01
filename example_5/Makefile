#简单赋值(:=)
x := foo
y := $(x)b
x := new

all:
	@echo x => $(x)
	@echo y => $(y)

#output:
$ make -n
echo x => new
echo y => foob


#递归赋值(=)
x = foo
y = $(x)b
x = new

all:
	@echo x => $(x)
	@echo y => $(y)

#output:
$ make -n
echo x => new
echo y => newb


