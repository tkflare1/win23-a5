# Compiler and flags
CC = gcc
CFLAGS = -Wall -Wextra -std=c99

# Source files and the corresponding object files
SRC = main.c addition.c subtraction.c multiplication.c division.c
OBJS = $(SRC:.c=.o)

# Name of the final executable
TARGET = calculator

# Default rule: build the binary
all: $(TARGET)

# Link all object files into the final executable
$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^

# Compile each .c file into a .o file
%.o: %.c operations.h
	$(CC) $(CFLAGS) -c $<

# Clean rule: remove all object files and the final executable
clean:
	rm -f $(OBJS) $(TARGET)

