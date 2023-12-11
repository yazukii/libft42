
# Libft

My own version of some functions of the standart C library (as well as some outside the standart C library). This project was made for educational purposes as part of the 42 Cursus.




## The functions in this project are:

- ### atoi
  - (short for ascii to int) Takes a string as argument and returns it as an int eg: "425" = 425
- ### itoa
  - (short for int to ascii) Takes a int as argument and returns it as an string eg: 425 = "425"
- ### bzero
  - Fills the first `n` bytes of an object with  zero (NUL) bytes
- ### calloc
  - Allocates `n` amount of memory and returns a pointer to it. Unlike `malloc()` `calloc()` fills that memory with zero (NUL) bytes
 - ### isalnum
    - check that the character is alphanumeric or not. It returns 1 if it is and zero otherwise. 
- ### isalpha
    - check that the character is alpha or not. It returns 1 if it is and zero otherwise. 
- ### isascii
    - check that the character is part of the  7–bit US-ASCII set or not. It returns 1 if it is and zero otherwise. 
- ### isdigit
  - check that the character is a digit or not. It returns 1 if it is and zero otherwise. 
- ### isprint
  - check that the character is a printable or not. It returns 1 if it is and zero otherwise
- ### memchr
  - Returns a pointer to the first occurence of c character in the `n` first bytes of object `s`
- ### memcmp
  - Compares the first `n` bytes of `s1` and `s2`. Returns `< 0` if `s1` is smaller than `s2`, `> 0` if `s1` is bigger than `s2` and `0` if `s1` is equal to `s2`.
- ### memcpy
  - Copies the first `n` bytes from `src` over to `dst`. It returns a pointer to `dst`.
- ### memmove
  - Copies the first `len` bytes from `src` over to `dst`. It returns a pointer to `dst`. It is safer than `memcpy()` because it copies `src` to a temporary buffer first before coying it to `src`. As a result `memcpy` can result in memory loss.
- ### memset
  - Copies `c` byte in place of the `len` first bytes of object `b`. Returns a pointer to `b`
- ### putchar
  - Prints the character `c` to the standard output with `write()`.
- ### putchar_fd
  - Prints the charcter `c` to the file `fd` with `write()`.
- ### putendl_fd
  - Prints the string `s` to the file `fd` with `write()`. It also adds a `\n` at the end.
- ### putstr_fd
  - Prints the string `s` to the file `fd` with `write()`.
- ### putstr
  - Prints the string `s` to the standard output with `write()`
- ### split
  - split the string `s` into multiple strings seperated by char `c`. Returns an array of string.
- ### strchr
  - Finds the first occurence of the character `c` in the string `s`. Returns a pointer to it or `NULL` if it was never found.
- ### strnchr
  - Finds the last occurence of the character `c` in the string `s`. Returns a pointer to it or `NULL` if it was never found.
- ### strdup
  - Duplicates the string `s1`. Returns a pointer to a duplicate of string `s1`.
- ### striteri
  - Applies the function `f` to each character of the string passed as argument, and passing its index as first argument. Each character is passed by address to `f` to be modified if necessary.
- ### strjoin
  - Concatenates `s1` and `s2` and returns the string resulting from this action.
- ### strlcpy
  - copies a string into a destination buffer by specifying the maximum size of the buffer to prevent overflow. It is safer than `strncpy` by guaranteeing to terminate the string with a null terminating character.
- ### strlcat
  - Appends string `s1` to the end of string `s2`, preventing buffer overflow by specifying the maximum size of the destination buffer. It is safer than `strncat` by guaranteeing to terminate the string with a null terminating character.
- ### strlen
  - Returns the length of string `str`.
- ### strmapi
  - Applies the function `f` to each character of the string `s`passed as argument by giving its index as first argument to create a “fresh” new string (with `malloc()`) resulting from the successive applications of `f`.
- ### strncmp
  - Compares the first `n` characters of string `s1` and `s2`. Returns `< 0` if `s1` is smaller than `s2`, `> 0` if `s1` is bigger than `s2` and `0` if `s1` is equal to `s2`.
- ### strnstr
  - Finds the first occurence of the substring `ndl` in the string `hs` within it's `len` first characters. Returns a pointer to the beginning of `ndl` in `hs`.
- ### strtrim
  - trims the set of character `set` from the beginning and end of `s1`. Returns the resulting string.
- ### substr
  - Allocates (with `malloc()`) and returns a “fresh” substring from the string `s`. The substring begins at index `start` and is of size `len`. If `start` and `len` aren’t refering to a valid substring, the behavior is undefined. If the allocation fails, the function returns NULL
- ### tolower
  - Returns charcter `c` as it's lowercase equivalent.
- ### toupper
  - Returns charcter `c` as it's uppercase equivalent.

## The next functions are related to linked lists.

- ### lstadd_back
  - Adds the node `new` at the end of the list.
- ### lstadd_front
  - Adds the node `new` at the beginning of the list.
- ### lstclear
  - Deletes and frees the given node and every successor of that node, using the function `del` and `free()`. Finally, the pointer to the list is set to `NULL`.
- ### lstdelone
  - Takes as a parameter a link’s pointer address and frees the memory of the link’s content using the function `del` given as a parameter, then frees the link’s memory using `free()`. The memory of next must not be freed under any circumstance. Finally, the pointer to the link that was just freed must be set to `NULL`.
- ### lstiter
  - Iterates the list `lst` and applies the function `f` to each link.
- ### lstlast
  - Iterates a list `lst` and applies the function `f` to each link to create a “fresh” list (using `malloc()`) resulting from the successive applications of `f`. If the allocation fails, the function returns `NULL`.
- ### lstmap
  - Iterates the list `lst` and applies the function `f` on the content of each node.  Creates a new list resulting of the successive applications of the function `f`.  The `del` function is used to delete the content of a node if needed.
- ### lstnew
  - Allocates (with `malloc()`) and returns a “fresh” link. The variables `content` and `content_size` of the new link are initialized by copy of the parameters of the function. If the parameter content is nul, the variable content is initialized to `NULL` and the variable `content_size` is initialized to `0` even if the parameter `content_size` isn’t. The variable `next` is initialized to `NULL`. If the allocation fails, the function returns `NULL`.
- ### lstsize
  - Returns the number of nodes in a list.
