CC			=gcc
CFLAGS		=-I.
DEPS 		= hellomake.h

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: hellomake.o hellofunc.o 
	$(CC) -o hellomake hellomake.o hellofunc.o 
clean:
	rm -rf hellomake hellomake.o hellofunc.o

# The -c flag says to generate the object file
# The -o flag says to put output file to the name on the left side of the :
# $@: 
# $<
