PROGRAM = EVEClocks

INCLUDEDIRS = \
	-I. \
	-I../include


LIBDIRS = \
	-L. \
	-L/usr/local/lib


#LIBS = /usr/local/lib/libftd2xx.so
LIBS = -L. -lmpsse -lftd2xx -lpthread -ldl -lrt -Wl,-rpath /usr/local/lib

CSOURCES = FT_App_Clocks.c FT_CoPro_Cmds.c FT_Gpu_Hal.c

# expands to list of object files
#COBJECTS = $(CSOURCES:.c=.o)  
CFLAGS = -Wall -g -Wfatal-errors
CC = gcc

LDFLAGS = $(LIBDIRS) $(LIBS)


all: $(PROGRAM)


$(PROGRAM): $(CSOURCES) 
	$(CC) $(CFLAGS)  $? $(INCLUDEDIRS) $(LIBS) -o $@ 

clean:
	$(RM) -f $(COBJECTS) $(PROGRAM) 

