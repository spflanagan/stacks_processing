README
coverage_from_stacks

Contact Sarah Flanagan (sflanagan@bio.tamu.edu) for more information.

This program takes stacks output and calculates coverage data and other summary statistics.
What it requires:
1. path to the directory containing the stacks *.matches.tsv files (one per individual)
2. text file in the same directory as this program with a list of the sample names (the part of the filenames preceding ".matches.tsv")

What it outputs:
1. Summary stats for each individual (e.g. average per-locus coverage, number of loci, etc.)
2. Summary stats for each locus (e.g. average per-individual coverage, number of individuals with that locus, etc.)
3. Overall summary stats (e.g. average per-locus coverage, average per-individual per-locus coverage, total number of loci, etc.)


Installation and Usage:
Windows:
Put the executable (coverage_from_stacks.exe) in a useful folder. It is easiest (the path you must provide is shortest) if you put it in your desired output directory.

Ubuntu:
Put the executable in a useful folder. It is easiest (the path you must provide is shortest) if you put it in your desired output directory.
**You may need to alter file permissions for it to run:
chmod u+x coverage_from_stacks

To run the file in interactive mode: 
./coverage_from_stacks

To run the file with arguments:
./coverage_from_stacks -p path/with/matches/files -i sample_id_list.txt -n output.txt

For help:
./coverage_from_stacks -h 

Other operating systems:
Compile the source code using the g++ compiler.
For example:
g++ coverage_from_stacks.cpp -o coverage_from_stacks -std=c++0x


Arguments:
-p: path to directory with stacks *.matches.tsv file
-i: List of sample IDs (the component of the filenames before the .matches.tsv)
-n: output name (e.g. pop ID, without any extensions; default = coverage)
-h: prints a help message
no arguments: interactive mode