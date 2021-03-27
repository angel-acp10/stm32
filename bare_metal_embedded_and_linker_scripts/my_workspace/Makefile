# CC stands for cross-compiler
CC = arm-none-eabi-gcc

# MACH stands for machine
MACH = cortex-m4

# compilation flags. $(MACH) is expanded to the variable value
# 	-c just compiles, do not link
# 	-mcpu= processor
#	-std= C language version/dialect
#	-O0 no optimization
CFLAGS = -c -mcpu=$(MACH) -mthumb -std=gnu11 -O0

# this will create two targets (main.o and led.o)
all: main.o led.o

# target: main.o
# dependency: main.c
# recipe: it is a command to create the target
# $@: same as target 
# $^: same as dependencies
main.o: main.c
	$(CC) $(CFLAGS) -o $@ $^

# target: led.o
# dependency: led.c
led.o: led.c
	$(CC) $(CFLAGS) -o $@ $^