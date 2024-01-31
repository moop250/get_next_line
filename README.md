# get_next_line
![](https://img.shields.io/badge/100%2F100-brightgreen)
## Description

`get_next_line` is a 42 project that requires the creation of a function to read content line by line from a file descriptor. The objective is to implement a way to read from a file or standard input and return one line at a time until the end of the file.

## Base Features

- Read and return a line from a file or standard input.
- Manage memory properly to prevent leaks.

## Compatibility & Size

![](https://img.shields.io/badge/WSL-0a97f5?style=for-the-badge&logo=linux&logoColor=white)
![](	https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=apple&logoColor=white)

![](https://img.shields.io/github/languages/code-size/hlibine/get_next_line?color=5BCFFF)

## Usage 

To clone the repository use:
```bash
git clone https://github.com/hlibine/get_next_line.git
```

Example usage in a C program:
```C
#include "get_next_line.h"

int main()
{
    int fd;
    char *line;

    fd = open("example_file.txt", O_RDONLY);
    while ((line = get_next_line(fd)) != NULL)
    {
        printf("%s", line);
        free(line);
    }
    close(fd);
    return (0);
}
```
