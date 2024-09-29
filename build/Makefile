# Compiler and flags
CC = gcc
CFLAGS = -Wall

# Directories
SRC_DIR = ../src
OBJ_DIR = ../obj
BUILD_DIR = .
INCLUDE_DIR = ../include

# Output binary
TARGET = $(BUILD_DIR)/cube_render

# Source and object files
SRCS = $(wildcard $(SRC_DIR)/*.c)
OBJS = $(SRCS:$(SRC_DIR)/%.c=$(OBJ_DIR)/%.o)

# Default target
all: $(TARGET)

# Rule for linking the binary
$(TARGET): $(OBJS)
	$(CC) $(OBJS) -lm -o $@

# Rule for compiling source files
$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c
	@mkdir -p $(OBJ_DIR)
	$(CC) $(CFLAGS) -c $< -o $@

# Clean up
clean:
	rm -rf $(OBJ_DIR)/*.o $(TARGET)

# Rebuild
rebuild: clean all

