# Flags
CXXFLAGS		= -std=c++11 -Wall -Wextra -g
# Comlpiler, tools and options
CXX 		   ?= g++
# executable # 
BIN_NAME 		= runner
# Define directories
SRC_PATH 		= src
BUILD_PATH 		= build
BIN_PATH 		= $(BUILD_PATH)/bin

INC_DIR			= include
INCPATH			= -I$(INC_DIR)

# Files
SOURCES			= Main.cpp Vector.cpp
OBJECTS			= $(patsubst %.cpp, $(BUILD_PATH)/%.o, $(SOURCES))


.PHONY: all clean
all: $(BUILD_PATH)/$(BIN_NAME)

$(BUILD_PATH)/%.o: $(SRC_PATH)/%.cpp
	@echo "Compiling $< -> $@"
	@$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

$(BUILD_PATH)/$(BIN_NAME): $(OBJECTS)
	@echo "Linking: $@"
	@$(CXX) -o $@ $^
clean:
	rm -rf build/*