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

SOURCES 	= $(shell find $(SRC_PATH) -name '*.c' | sort -k 1nr | cut -f2-)
OBJ 		= $(patsubst %.c, $(DEST_DIR)/%.o, $(SOURCES))
OBJECTS		= $(SOURCES:$(SRC_PATH)/%.c=$(DEST_DIR)/%.o)  


.PHONY : all clean
all: $(DEST_DIR)/$(BIN_NAME)

test:
	echo $(OBJECTS)

$(DEST_DIR)/%.o: $(SRC_PATH)/%.c
	$(CC) -c -o $@ $< $(CFLAGS)

$(DEST_DIR)/$(BIN_NAME): $(OBJECTS)
	$(CC) -o $@ $^
clean:
	rm -rf bin/*
