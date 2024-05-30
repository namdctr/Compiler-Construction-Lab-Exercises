CPP      = g++.exe
CC       = gcc.exe
WINDRES  = windres.exe
OBJ      = main.o charcode.o error.o parser.o reader.o scanner.o token.o
LINKOBJ  = main.o charcode.o error.o parser.o reader.o scanner.o token.o
LIBS     = -L"C:/msys64/ucrt64/lib" -L"C:/msys64/ucrt64/x86_64-w64-mingw32/lib" -static-libgcc
INCS     = -I"C:/msys64/ucrt64/include" -I"C:/msys64/ucrt64/lib/gcc/x86_64-w64-mingw32/13.2.0/include"
CXXINCS  = -I"C:/msys64/ucrt64/include" -I"C:/msys64/ucrt64/lib/gcc/x86_64-w64-mingw32/13.2.0/include" -I"C:/msys64/ucrt64/lib/gcc/x86_64-w64-mingw32/13.2.0/include/c++"
BIN      = parser.exe
CXXFLAGS = $(CXXINCS) 
CFLAGS   = $(INCS) 
RM       = rm.exe -f

.PHONY: all all-before all-after clean clean-custom

all: all-before $(BIN) all-after

clean: clean-custom
	${RM} $(OBJ) $(BIN)

$(BIN): $(OBJ)
	$(CC) $(LINKOBJ) -o $(BIN) $(LIBS)

main.o: main.c
	$(CC) -c main.c -o main.o $(CFLAGS)

charcode.o: charcode.c
	$(CC) -c charcode.c -o charcode.o $(CFLAGS)

error.o: error.c
	$(CC) -c error.c -o error.o $(CFLAGS)

parser.o: parser.c
	$(CC) -c parser.c -o parser.o $(CFLAGS)

reader.o: reader.c
	$(CC) -c reader.c -o reader.o $(CFLAGS)

scanner.o: scanner.c
	$(CC) -c scanner.c -o scanner.o $(CFLAGS)

token.o: token.c
	$(CC) -c token.c -o token.o $(CFLAGS)
