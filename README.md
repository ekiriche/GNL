# GNL
This project will not only allow you to add a very convenient function to your collection,
but it will also allow you to learn a highly interesting new concept in C programming:
static variables.
You will also gain a deeper understanding of allocations, whether they happen on the
stack memory or in the heap memory, the manipulation and the life cycle of a buffer, the
unexpected complexity implied in the use of one or many static variables.

## Allowed functions
1. `malloc`
2. `read`
3. `free`

## Mandatory part
1. Write a function that returns a line read from a file descriptor.
2. What we call a “line” is a succession of characters that end with ’\n’ (ascii code
0x0a) or with End Of File (EOF).
3. Your function must be prototyped as follow : `int get_next_line(const int fd, char **line);`
4. The first parameter is the file descriptor that will be used to read.
5. The second parameter is the address of a pointer to a character that will be used
to save the line read from the file descriptor.
6. The return value can be 1, 0 or -1 depending on whether a line has been read,
when the reading has been completed, or if an error has happened respectively.
7. Your function get_next_line must return its result without ’\n’.
8. Calling your function get_next_line in a loop will then allow you to read the text
available on a file descriptor one line at a time until the end of the text, no matter
the size of either the text or one of its lines.
9. Make sure that your function behaves well when it reads from a file, from the
standard output, from a redirection etc.
10. We consider that get_next_line has an undefined behavior if, between two calls,
the same file descriptor designs two distinct files although the reading from the first
file was not completed.
11. We consider also that a call to lseek(2) will never take place between two calls of
the function get_next_line on the same file descriptor.
12. Finally we consider that get_next_line has an undefined behavior when reading
from a binary file. However, if you wish, you can make this behavior coherent.
13. Global variables are forbidden.
14. Static variables are allowed.

## Final grade - 125/100(max)
