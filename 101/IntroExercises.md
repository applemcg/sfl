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


