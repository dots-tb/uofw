# Copyright (C) 2011, 2012 The uOFW team
# See the file COPYING for copying permission.

CFLAGS=-Wall -Wextra -Werror
LDFLAGS=
TARGET=psp-fixup-imports
OBJECTS=../common/sha1.o psp-fixup-imports.o

all: $(TARGET)

$(TARGET): $(OBJECTS)
	@echo "Creating binary $(TARGET)"
	@$(CC) $(OBJECTS) -o $@ $(LDFLAGS)

%.o: %.cpp
	@echo "Compiling $^"
	$(CC) $(CFLAGS) -c $^ -o $@

clean:
	@echo "Removing all the .o files"
	@$(RM) $(OBJECTS)

mrproper: clean
	@echo "Removing binary"
	@$(RM) $(TARGET)

