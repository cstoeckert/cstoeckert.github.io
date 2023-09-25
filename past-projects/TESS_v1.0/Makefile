OPTIONS  = -O3 -w
CC       = cc
LIBRARIES =  -lm

all:  tessWms

touch:
	touch *.c

clean:
	rm tessWms

tessWms: tessWms.c
	${CC} ${OPTIONS} -o tessWms tessWms.c ${LIBRARIES}

