CC = gcc
CFLAGS = -Wall -g

libprint.so: print.c
	$(CC) $(CFLAGS) -fpic -shared print.c -o libprint.so
	sudo mv libprint.so /lib

all: main.o libprint.so
	$(CC) $(CFLAGS) main.o  -l print  -o output

main.o: main.c
	$(CC) $(CFALGS) -c main.c

clean:
	rm *.o output libprint.so
