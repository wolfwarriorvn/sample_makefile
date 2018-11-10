# Compiler, tools and options
CC			=gcc

# Executable 
BIN_NAME = app

# Define the directories.
DEPS 		= hellomake.h
DEST_DIR	= ./bin
SRC_PATH	= ./src

INC_DIR		= ./include
CFLAGS		= -I$(INC_DIR)

# Files
SOURCE 		= hellofunc.c hellomake.c
OBJ 		= $(patsubst %.c, $(DEST_DIR)/%.o, $(SOURCE))  


.PHONY : all clean
all: $(DEST_DIR)/$(BIN_NAME)

$(DEST_DIR)/%.o: $(SRC_PATH)/%.c
	$(CC) -c -o $@ $< $(CFLAGS)

$(DEST_DIR)/$(BIN_NAME): $(OBJ)
	$(CC) -o $@ $^
clean:
	rm -rf bin/*
