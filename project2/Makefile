arm-as := arm-elf-as
arm-ld := arm-elf-ld
asflags := -g
ldflags := -g

myprintf: myprintf.o main.o sys.o myscanf.o
	$(arm-ld) $(ldflags) -Ttext=0 sys.o myscanf.o main.o myprintf.o -o myprintf
myprintf.o: myprintf.s
	$(arm-as) $(asflags) myprintf.s -o myprintf.o
main.o: main.s
	$(arm-as) $(asflags) main.s -o main.o
myscanf.o: myscanf.s
	$(arm-as) $(asflags) myscanf.s -o myscanf.o
clean:
	-rm myprintf.o main.o myprintf
