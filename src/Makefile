CC = gcc
FLAGS = -Wall -Werror -Wextra

all: print_module documentation_module

print_module: main_module_entry_point.o print_module.o
	$(CC) $(FLAGS) main_module_entry_point.o print_module.o -o ../build/Quest_1

 main_module_entry_point.o:  main_module_entry_point.c 
	$(CC) $(FLAGS) -c main_module_entry_point.c 

print_module.o: print_module.c
	$(CC) $(FLAGS) -c print_module.c

documentation_module: main_module_entry_point.o documentation_module.o
	$(CC) $(FLAGS) main_module_entry_point.o documentation_module.o -o ../build/Quest_2

documentation_module.o: documentation_module.c
	$(CC) $(FLAGS) documentation_module.c

check:
	cppcheck --check-config --enable=all --suppress=missingIncludeSystem ./

clean:

	rm -f *.o

	rm ../build/Quest_*

rebuild: clean all
