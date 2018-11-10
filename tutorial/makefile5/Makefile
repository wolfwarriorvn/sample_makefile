# Compiler, tools and options
CC			=gcc
# Path
DEPS 		= hellomake.h
OBJ			= ./bin/hellomake.o ./bin/hellofunc.o
DEST_DIR	= ./bin
SRC_PATH	= ./src
# Executable 
BIN_NAME = hellomake

INC_DIR		= ./include
CFLAGS		= -I$(INC_DIR)


.PHONY : all clean
all: $(DEST_DIR)/$(BIN_NAME)

$(DEST_DIR)/%.o: $(SRC_PATH)/%.c
	$(CC) -c -o $@ $< $(CFLAGS)

$(DEST_DIR)/$(BIN_NAME): $(OBJ)
	$(CC) -o $@ $^
clean:
	rm -rf bin/*
