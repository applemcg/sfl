

# Shell Function Library 101

[Table of Contents](../index.md)

This is the introductory lesson to Shell Libraries.  It is made up of
a handful of specific functions with a few thrown in as place-holders
for follow-up lessons.

The command-line examples assume the user is in the 101 directory of the [slf REPO]{ ... ) 
The accompanying local links refer to files in this document.


!include ./101/IntroExercises.md

!include ./101/NewConcepts.md

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







