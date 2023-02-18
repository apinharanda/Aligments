# Aligments

There are several different ways to align whole genomes and which one to use depends on the reason: we dont always align to ref
This rep has a collection of several different kinds of alignments we use in a regular basis

The nature of MUMmer is to chain together "maximal unique matches", so at its core it relies on those small stretches of hits. It is very fast, and has a good visual output
It is terrible to actually get the sequences

other approaches to whole-genome alignment that can alleviate this constraint to varying extents

If your sequences/genomes aren't super diverged use minimap2 with the -x asm5 or -x asm20 presets, and make sure to use the -a, -L, and --cs arguments to output as SAM and include the tags that would be useful for reconstruction of the aligned sequences (and also force base-level alignment)

Alternatively, there's also LAST (see the command recipes here for examples: https://github.com/mcfrith/last-genome-alignments), although the output format is MAF (which can be a bit rough to parse) and may be somewhat fragmented.

There are some other options for whole genome alignment (e.g. SibeliusZ)

Orthofinder - is not a whole genome alignment, but is an alignment for protein sequences for different species
