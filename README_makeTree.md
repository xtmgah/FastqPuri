# makeTree user manual

Reads a `fasta` file, creates a tree structure of a predefined 
depth `DEPTH` and saves it to a file. 

**NOTE**: computing a tree from a fasta file is very memory 
intensive. The program will not compute a tree if the length of the 
sequences in the fasta file exceeds 10 MB. Nevertheless, be 
careful with the `DEPTH`. The longer the `DEPTH`, the larger the tree
structure. The memory roof for the tree was set to XXXXXXXXXXXXX. 
If you want to change it, you can set the variable when calling 
`cmake` by passing the option `-DMEM_ROOF=<yourmemoryroof>`

**NOTE:** I might improve this. I have to decide how to set the 
memory roof!

## Running the program

Usage `C` executable (in folder `bin`): 

```
Usage: ./makeTree -f|--fasta <FASTA_INPUT> -l|--depth <DEPTH> 
-o, --output <OUTPUT_FILE> Reads a *fa file, constructs a tree of 
depth DEPTH and saves it compressed in OUTPUT_FILE.
Options: 
 -v, --version Prints package version.
 -h, --help    Prints help dialog.
 -f, --fasta   Input folder containing *bin data (output from Qreport). Mandatory option.
 -l, --depth depth of the tree structure
 -o, --output Output file. If the extension is not *gz, it is added. Mandatory option.
 -o Output file (with NO extension). Mandatory option.
```


## Output description

Compressed file containing the tree structure. For further details,
read the `Doxygen` documentation of the file `tree.c`, function `save_tree`.

## Example 
 
TODO

## Contributors

Paula Pérez Rubio 

## License

GPL v3 (see LICENSE.txt)