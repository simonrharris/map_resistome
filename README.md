# map_resistome

PLEASE NOTE: THIS SCRIPT IS DEPRECATED. WE RECOMMEND THE USE OF ARIBA (https://github.com/sanger-pathogens/ariba) INSTEAD.

A python script for identifying matches to resistance alleles in genome assemblies. Unlike many other methods map_resistome will highlight partial matches at contig boundaries that may be the result of assembly issues for repetitive resistance genes.

Requirements:

Requires local intallations of SMALT and samtools. If these are not in your default PATH, please edit the SMALT_DIR and SAMTOOLS_DIR locations in the two python files.

Usage: 
map_resistome.py [options]

Options:<BR>
--version             show program's version number and exit<BR>
-h, --help            show this help message and exit<BR>
-c FILE, --contigs=FILE multifasta containing contigs to search in<BR>
-f FILE, --forward=FILE forward fastq file (may be zipped, but must end .gz)<BR>
  -r FILE, --reverse=FILE
                        reverse fastq file (may be zipped, but must end .gz)<BR>
  -g FILE, --genes=FILE
                        multifasta containing genes to search for<BR>
  -o FILE, --output=FILE
                        output prefix<BR>
  -i float, --id=float  minimum id to report match (excluding clipping due to
                        contig breaks). Must be between 0 and 1. [default =
                        0.9]
