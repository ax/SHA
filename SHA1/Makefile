# Compiling macros
CC = gcc
OPT = -Wall -Wno-pointer-sign -D _DEFAULT_SOURCE -D_XOPEN_SOURCE=700 -D_REENTRANT -DPURIFY -O3 #_BSD_SOURCE  
COMP = $(CC) $(OPT)

# working directories
DIR = /tmp/SHA1/
HERE = ./

OBJS = sha1.o 

sha1_test: $(HERE)sha1test.c $(OBJS)
	$(COMP)	-o $@ $(HERE)sha1test.c $(DIR)sha1.o

sha1.o: $(HERE)sha1.c
	$(COMP) -o $(DIR)$@ -c $(HERE)sha1.c 

clean:
	rm $(DIR)*.o
	rm sha1test
