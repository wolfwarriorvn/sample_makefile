CC			=gcc
CFLAGS		=-I.
DEPS 		= hellomake.h
OBJ			= hellomake.o hellofunc.o

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	$(CC) -o $@ $^
clean:
	rm -rf hellomake hellomake.o hellofunc.o
