OBJS = MainFunction.o ClientUtility.o HandleUtility.o RTPPacketUtility.o LayoutUtility.o CallbackUtility.o 
CC = gcc
CFLAGS = -Wall -O -g
PKGCON = `pkg-config --cflags --libs gtk+-2.0`
TARGET = ./VideoClient

# Compile .c file to .o file
%.o : %.c
	$(CC) $(CFLAGS) -c $< -o $@ $(PKGCON)

# Get all .c files
SOURCES = $(wildcard *.c)
# Replace .c file by .o file
OBJS = $(patsubst %.c, %.o, $(SOURCES))

# Link all .o files
$(TARGET) : $(OBJS)
	$(CC) $(OBJS) -o $(TARGET) $(PKGCON)
	chmod a+x $(TARGET)

clean:
	rm -rf *.o VideoClient
