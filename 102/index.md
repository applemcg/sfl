

# Shell Function Library 102

This lessons adds debugging support functions to the SFL collection.
Features have **on** and **off** function handles which work from the 
commaneline an within functions.    

# What's Here

The sfl_list gets a replecement upgrade in this library.  It anticipates
the function collection called *function families*

## New Functions

+ debug -- debug{,_{,on,off}}
* pause -- pause{,_{,on,off}}

# Mzintenance, Direction

## Concepts

NNN  concepts appear here which may be new to you, and will be
expanded upon in future editions of Shell Library lessons.


1. the **null command**, in this case the line:

       : Shell Library 101, library function list;
       : where the leading colon starts the null command

    here is [the Null Command](https://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html), where the first example is appropriate
	
       : (a colon)
    
1. [the ${*:-echo} idiom](https://www.gnu.org/software/bash/manual/bash.html#Shell-Parameter-Expansion)   where the example is:

        : ${parameter:-word}
        
1. [curly brace { ,,, } expansion](https://www.gnu.org/software/bash/manual/bash.html#B
race-Expansion)  where the example, under **Brace Expansion**

        $ echo a{d,c,b}e
        ade ace abe
        
1. Using an underscore, e.g. `sfl_init` in function names introduces
   the concept of a function `family`, in this case **sfl** is the
   family and *init* is the subfunction. Many subfunction names such
   as `init, help, list` as used here to handle family administrative
   functions.

These tags are used throughout my function repertoire, where the null
command adds these features to any function:

+ tags -- such as date, related, lesson, usage, example, ..
+ datestamp -- the date tag
+ abstract -- the first null-command line, see abstracts.txt
+ shdoc -- the null-command lines before the first tag.

There are necessary precautions in using the null-command which will
be covered in a later lesson.

## Contact the Author

+ name:  [Marty McGowan](mailto:martymcgowan@alum.mit.edu)
+ about: http://mcgowans.org/marty3
+ page:  http://mcgowans.org/marty3/sfl
+ text: <a href="./index.md" download="index.md">document source</a>







