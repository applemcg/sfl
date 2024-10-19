

# Shell Function Library 101

This is the introductory lesson to Shell Libraries.  It is made up of
a handful of specific functions with a few thrown in as place-holders
for follow-up lessons.


# Work Exercises to Get Acquainted

The command-line examples assume the user is in the 101 directory; the
accompanying links take advantage of this document.

Before sourcing the shell library, inspect the abstracts.txt file.

        $ cat abstracts.txt  # or

   <a href="./abstracts.txt" download="abstracts.txt">Download abstracts.txt</a>

It's possible to view function two ways:

1. view the library in a view-only editor 

        $ view $(which sfl101.lib) 
		
   <a href="./sfl101.lib" download="sfl101.lib">Download sfl101.lib</a>
   
1. source the library in a sub-shell and display a function body

Since the latter means may be new to you, here's how:

        $ ( source $(which sfl101.lib); 
            declare -f sfl_help )    # the parens define the sub-shell

Alternatively,

        $ ( source $(which sfl101.lib); 
		    declare -f fbdy )  ;     # you see the function

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

# Maintenance, Direction

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

## Concepts

Four concepts appear here which may be new to you, and will be
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
        
+ name:  [Marty McGowan](mailto:martymcgowan@alum.mit.edu?subject=Subject%20Function%20Libraries)
+ about: http://mcgowans.org/marty3
+ page:  http://mcgowans.org/marty3/sfl
+ text: <a href="./index.md" download="index.md">document source</a>







