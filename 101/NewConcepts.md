# Concepts

Four concepts appear here which may be new to you, and will be
expanded upon in future editions of Shell Library lessons.

1. A function's ``abstract`` is taken from a **null command**,  the first line:

       : Shell Library 101, library function list;

    This document introduces [the Null Command](https://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html).   The first example is appropriate:
	
       : (a colon)
	   
	   
   1. A ``smart_list`` is built using the **default argument** using
      an [${*:-echo}
      idiom](https://www.gnu.org/software/bash/manual/bash.html#Shell-Parameter-Expansion)
      where the example is:

        : ${parameter:-word}
        
1. [curly brace { ,,, } expansion](https://www.gnu.org/software/bash/manual/bash.html#B
race-Expansion)  where the example, under **Brace Expansion**

        $ echo a{d,c,b}e
        ade ace abe

1. A function may have searchable ``tag``s,  which is also built from a null command.
   A tag looks like
   
       : *tagname: optional data ...*

      
   with examples:


+ date: *2024-11-12 ... ;*
+ related: *func_a, cmd_c, ...* lesson, 
+ usage:   *~ argname, ...*
+ todo:  *a planned enhancement ...*
+ bug:  *todo today?*

with these functions to retrieve the first null command lines

+ abstract -- the first null-command line
+ shdoc -- all tthe null-command lines before a tag or non-null commanf=d.

There are necessary precautions in using the null-command which will
be covered in a later lesson.
