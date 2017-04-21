PROGRAM = EVEClocks

INCLUDEDIRS = \
	-I. \
	-I../include

INC = ../include/

LIBDIRS = \
	-L. \
	-L/usr/local/lib


#LIBS = /usr/local/lib/libftd2xx.so
LIBS = -L. -lmpsse -lftd2xx -lpthread -ldl -lrt -Wl,-rpath /usr/local/lib

CSOURCES = FT_App_Clocks.c FT_CoPro_Cmds.c FT_Gpu_Hal.c
HSOURCES = $(INC)FT_CoPro_Cmds.h \
		   $(INC)FT_DataTypes.h \
		   $(INC)FT_Gpu_Hal.h \
		   $(INC)FT_Hal_Utils.h \
		   $(INC)FT_Platform.h \
		   $(INC)WinTypes.h \
		   $(INC)ftd2xx.h

# expands to list of object files
#COBJECTS = $(CSOURCES:.c=.o)  

CFLAGS = -Wall -g -Wfatal-errors 
CC = gcc

LDFLAGS = $(LIBDIRS) $(LIBS)


all: $(PROGRAM) $(CSOURCES) $(HSOURCES)



$(PROGRAM): $(CSOURCES) $(HSOURCES)
	$(CC) $(CFLAGS)  $(CSOURCES) $(INCLUDEDIRS) $(LIBS) -o $@ 


clean:
	$(RM) -f $(COBJECTS) $(PROGRAM) 


#$(CC) $(CFLAGS)  $? $(INCLUDEDIRS) $(LIBS) -o $@ 

