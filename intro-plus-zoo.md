# 1.4.1: Why learn to program in C?
	
### It's a de facto substandard of languages, runs on all hardware, and gives you the most control over your system, imposing few constraints, leading to the ability to write programs that would be difficult in higher level languages.

# 1.42: Why learn about data structures and programming techniques?

### Representing real world data requires thinking about how to organize it, which will subsequently benefit the overall organization of your program(s).

### C does not provide tools for such data organization out of the box, as some languages do, which means building them is your responsibility: because they're predicated on concepts such as pointers and storage allocation, doing so will require attaining, and provide a much deeper understanding of how computers operate.

# 2.5.1/2: Creating, compiling and running a program.

### A file saved with the extension `c` will indicate to a C compiler (or syntax highlighter) that the contexts are C source, for example:

```C
#include <stdio.h>

int
main(int argc, char **argv) {
    int i;

    puts("Now I will count from 1 to 10");

    for(i = 1; i <= 10; i++) {
        printf("%d\n", i);
    }

    return 0;
}
```
```
overoxidize@oxhq:$ gcc -g3 -o count count.c

overoxidize@oxhq:$ ./count

Now I will count from 1 to 10.
1
2
3
4
5
6
7
8
9
10
```

`gcc` is the command to start the gnu C compiler, which will compile the file, with maximum debugging info due to `-g3`. 

`-o` allows you to specify the name of the output file, which is followed by the file name of your choice, and finally `count.c` is the name of the file we want to compile according to these *flags*: meaningful strings that alter the behavior of the command line program we're using, as we choose.


### Originally, I wrote the return statement in the body of the for loop, causing the program to exit on the first iteration of the loop, which lead to a surprising (and amusingly contradictory):



```
overoxidize@oxhq:$ gcc -g3 -o count count.c

overoxidize@oxhq:$ ./count

Now I will count from 1 to 10.
1
```

# 2.5.3: Notes on what the program does.

### `#include <std.io>` brings in declarations for the basic input/output behaviors, such as `puts` and `printf`,

### int main(int argc, char **argv)