CC = cc
CXX = c++
EXE = exe

all: $(EXE)

$(EXE): hello.o
	$(CXX) main.cpp $^ -o $@

hello.o: hello.c hello.h
	$(CC) -c $< -o $@

clean:
	rm -f *~ *.o $(EXE)

.PHONY: all clean format

format: hello.c hello.h main.cpp 
	@clang-format -i $^ 2>/dev/null || echo "Please install clang-format to run this commands"
