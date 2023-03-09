# octave
All the arrays and matrices used are dinamically alocated in memory, using malloc(), realloc() and free() functions from the stdlib.h library.

I defined 2 data types: "dim" (that stores 2 ints - the no. of lines and columns of a matrix) and "pack" (that stores the array of matrices, the array of matrix dimensions and the number of matrices present in the array)

I always give my_pack (the bundle of matrices, dimensions and their size) as parameter in the functions because I have to check whether malloc() or realloc() fails. In case it does, I have to free all the memory I allocated, so I need to have acces to the arrays.

In the main() function, I initially allocate space for 10 elements in the matrices and dimensions arrays

There are 10 possible commands that can be recieved from input:

'L' - Loads a matrix with the given sizes and values into the memory
'D' - Prints the no. of lines & columns of the matrix at the given index
'P' - Prints the values present in the matrix at the given index
'C' - Resizes the matrix based on the given instructions
'M' - Multiplies two matrices, adding the resulted matrix into memory
'O' - Sorts the matrices in ascending order, based on the sum of their values
'T' - Transposes the matrix at the given index
'F' - Frees the matrix at a given index
'S' - Multiplies two square matrices using the Strassen algorithm
'Q' - Frees all the memory alocated and stops the program
