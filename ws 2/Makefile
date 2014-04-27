SRCDIR=src/
BINDIR=bin/
# Include files
SOURCES=initLB.c visualLB.c boundary.c collision.c streaming.c computeCellValues.c main.c helper.c
# Compiler
# --------
CC=gcc

CFLAGS=-Werror -pedantic -Wall

# Linker flags
# ------------
LDFLAGS= 

OBJECTS=$(SOURCES:.c=.o)
BINOBJECTS=$(patsubst %.o,$(BINDIR)%.o,$(OBJECTS))
EXECUTABLE=lbsim

all: $(EXECUTABLE)


$(EXECUTABLE): $(OBJECTS)
	$(CC) $(BINOBJECTS) -o $@ $(LDFLAGS)

clean:
	rm -f $(BINOBJECTS) $(EXECUTABLE)

$(OBJECTS): %.o : $(SRCDIR)%.c
	$(CC) $(CFLAGS) -c $< -o $(BINDIR)$@ 
