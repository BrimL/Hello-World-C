IDIR =../include
CC=gcc
CFLAGS=-I$(IDIR)
EXECUTABLE=HelloWorld

ODIR=../obj
LDIR =../lib

_DEPS = helloworld.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = helloworld.o helloworldfunc.o holdscreenfunc.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))


$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

$(EXECUTABLE) : $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~