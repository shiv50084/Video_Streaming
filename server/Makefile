OBJS = MainFunction.o Thread.o ServerUtility.o AddressUtility.o HandleRequestUtility.o RTPPacketUtility.o SendUtility.o TimeUtility.o StringUtility.o 
LIBS = -lpthread
CC = gcc
CFLAGS = -Wall -O -g
TARGET = ./VideoServer

# Compile .c file to .o file
%.o : %.c
	$(CC) $(CFLAGS) -c $< -o $@

# Get all .c files
SOURCES = $(wildcard *.c)
# Replace .c file by .o file
OBJS = $(patsubst %.c, %.o, $(SOURCES))

# Link all .o files
$(TARGET) : $(OBJS)
	$(CC) $(OBJS) -o $(TARGET) $(LIBS)
	chmod a+x $(TARGET)

clean:
	rm -rf *.o VideoServer
