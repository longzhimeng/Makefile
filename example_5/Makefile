#简单赋值(:=)常规的赋值方式，一赋值马上有效。在没赋值是为空字符。
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


#递归赋值(=):赋值后并不马上生效，等到使用时才真正的赋值
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

