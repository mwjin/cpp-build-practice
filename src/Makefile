CC = g++
CXXFLAGS = -g -Wall -std=c++17
OBJS = foo.o bar.o main.o

foo.o: foo.h foo.cpp
	$(CC) $(CXXFLAGS) -c foo.cpp

bar.o: bar.h bar.cpp
	$(CC) $(CXXFLAGS) -c bar.cpp

main.o: main.cpp foo.h bar.h
	$(CC) $(CXXFLAGS) -c main.cpp

main: foo.o bar.o main.o
	$(CC) $(CXXFLAGS) $(OBJS) -o main

.PHONY: clean
clean:
	rm -f $(OBJS) main
