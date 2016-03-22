# Compilador que será utilizado
CC=g++

# flags de compilación
CFLAGS=-g -Wall -O2 -std=c++11

SOURCES=KaioKenSolver.cpp GenkidamaSolver.cpp KamehamehaSolver.cpp

# Objetos que serán generados (no tocar)
OBJECTS=$(SOURCES:.cpp=.o)

# Nombre de ejecutables a generar
EXECUTABLES=KaioKenSolver GenkidamaSolver KamehamehaSolver

.PHONY: all clean

all: clean $(SOURCES) $(EXECUTABLES)

# KAIOKEN

KaioKenSolver: KaioKenSolver.o
	$(CC) $@.o -o $@

runKaioKenSolver: cleanKaioKenSolver KaioKenSolver
	./KaioKenSolver

cleanKaioKenSolver:
	rm -rf KaioKenSolver KaioKenSolver.o

# GENKIDAMA

GenkidamaSolver: GenkidamaSolver.o
	$(CC) $@.o -o $@

runGenkidamaSolver: cleanGenkidamaSolver GenkidamaSolver
	./GenkidamaSolver

cleanGenkidamaSolver:
	rm -rf GenkidamaSolver GenkidamaSolver.o

# KAMEHAMEHA

KamehamehaSolver: KamehamehaSolver.o
	$(CC) $@.o -o $@

runKamehamehaSolver: cleanKamehamehaSolver KamehamehaSolver
	./KamehamehaSolver

cleanKamehamehaSolver:
	rm -rf KamehamehaSolver KamehamehaSolver.o

# TODOS

clean:
	rm -rf $(EXECUTABLES) $(OBJECTS)

#valgrind: $(EXECUTABLES)
#	valgrind --leak-check=full --track-origins=yes ./$(EXECUTABLES)

.cpp.o:
	$(CC) $(CFLAGS) $< -c -o $@