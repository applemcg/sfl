

# Shell Function Library 101

[Table of Contents](../index.md)

This is the introductory lesson to Shell Libraries.  It is made up of
a handful of specific functions with a few thrown in as place-holders
for follow-up lessons.

The command-line examples assume the user is in the 101 directory of the [slf REPO]{ ... ) 
The accompanying local links refer to files in this document.

# Introduction,  Work Exercises

Prepare with

> $ cd 


## The Abstract 

To see a brief synopsis of a function collection, collect their ``abstract``s,
which are taken fro m the first comment line of a shell function.
Here is a tasble of the functions in this shell library, *./sfl101.lib*,

        $ cat abstracts.txt  # or

   <a href="./abstracts.txt" download="abstracts.txt">Download abstracts.txt</a>
   
## To see single library function, start with a ``smart_list``, in
    this case, **slf101_list**, view the library in a view-only editor

        $ view +/sfl101_list/  ./sfl101.lib # or follow this link
		
   <a href="./sfl101.lib" download="sfl101.lib">Download sfl101.lib</a>
   
    or equivalently, source the library in a sub-shell to display a function body

        $ ( source $(which sfl101.lib); 
            declare -f sfl_help )    # the parens define the sub-shell


# Concepts

Four concepts appear here which may be new to you, and will be
expanded upon in future editions of Shell Library lessons.

1. A function's ``abstract`` is taken from a **null command**,  the first line:

       : Shell Library 101, library function list;

    This document introduces [the Null Command](https://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html).   The first example is appropriate:
	
       : (a colon)
	   
	   
   1. A ``smart_list`` is built using the **default argument** using an [${*:-echo} idiom](https://www.gnu.org/software/bash/manual/bash.html#Shell-Parameter-Expansion)   where the example is:

        : ${parameter:-word}
        
1. [curly brace { ,,, } expansion](https://www.gnu.org/software/bash/manual/bash.html#B
race-Expansion)  where the example, under **Brace Expansion**

        $ echo a{d,c,b}e
        ade ace abe




1. A function may have searchable ``tag``s,  which is also built from a null command.
   A tag looks like
   
   //: tagname: optional data ... ;//
   
   with examples:


+ date: //2024-11-12 ... ;
+ related: //func_a, cmd_c, ... // lesson, 
+ usage:  //~ argname, ... //
+ todo:  //a planned enhancement ... //
  + bug:  //todo today? //

with these functions to retrieve the first null command lines

+ abstract -- the first null-command line
+ shdoc -- all tthe null-command lines before a tag or non-null commanf=d.

There are necessary precautions in using the null-command which will
be covered in a later lesson.

# Exercises

By inspecting the library completely, satisfy yourself you are
comfortable in allowing it's contents into your shell environment.
Simply conduct these steps:

	$ source $(which sfl101.lib) # and begin to examine its features
    $ fbdy                       # with no arguments
	$ sfg1 ...                   # Set Functions Group ...,  e.g.
	$ sfg1 sfl_                  # names and uses of sfl_
	$ sfl_list fbdy              # you will likely need to Pipe it
	$ sfl_list fbdy | more       # and as a reminder;
	$ sfl_help                   # importantlty, for future maintenance
	$ fbdy sfl_init              # shows the sfl_init function, which
		                         # overwrites a local ./ copy of sfl101.li

## Maintenance, Direction

The latter step suggests that to add a function to the library, the
local copy anyway, you need to add the function to the `sfl_list`,
shown here:

```
    sfl_list () 
    { 
        : Shell Library 101, library function list;
        ${*:-echo} sfg1 functions fbdy comment debug pause \
                   sfl_{help,init,list}
    }
```
# Contact the Author
        
+ name:  [Marty McGowan](mailto:martymcgowan@alum.mit.edu?subject=Subject%20Function%20Libraries)
+ about: http://mcgowans.org/marty3
+ page:  http://mcgowans.org/marty3/sfl
+ text: <a href="./index.md" download="index.md">document source</a>







