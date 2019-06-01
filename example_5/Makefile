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


#条件赋值(?=)
x := foo
y := $(x)b
x ?= new

all:
	@echo x => $(x)
	@echo y => $(y)

#output:
$ make -n
echo x => foo
echo y => foob



#追加赋值(+=)
x := foo
y := $(x)b
x += $(y) 

all:
	@echo x => $(x)
	@echo y => $(y)

#output:
$ make -n
echo x => foo foob
echo y => foob

