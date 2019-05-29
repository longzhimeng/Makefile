CFLAGS=-g -O3
CXXFLAGS=-ggdb3 -O0 
CPPFLAGS=-DX=1 -DY=2

#CXX default value = g++
main_cpp: main_cpp.cpp
	$(CXX) $(CXXFLAGS) $(CPPFLAGS) $< -o $@
	@echo === make ok, output: $@ ===

#CC default value = cc
main_c: main_c.c
	$(CC) $(CFLAGS) $(CXXFLAGS) $< -o $@ 
	@echo === make ok, output: $@ ===

#clean project
.PHONY: clean
clean:
	$(RM) main_c main_cpp  *.o

