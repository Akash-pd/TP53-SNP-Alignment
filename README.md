# Detecting a TP53 Point Mutation with Biopython

## About This Project
I wrote this script to practice automating genetic sequence analysis with Python. It is a straightforward bioinformatics pipeline that detects a Single Nucleotide Polymorphism (SNP) in the *TP53* tumor suppressor gene by aligning a "patient" sample against a healthy reference sequence.

## The Biology Behind the Code
Coming from a wet-lab and clinical background, I know how crucial it is to quickly identify mutations in genes like *TP53* for cancer diagnostics. This code simulates the computational step right after DNA sequencing: finding exactly where the patient's DNA differs from the wildtype genome. 

## Tools Used
* **Language:** Python
* **Library:** Biopython (`Bio.Align`, `Bio.SeqUtils`)
* **Algorithm:** Global Pairwise Sequence Alignment

## What the Script Does
1. **Loads the DNA:** Sets up the wildtype and mutated DNA strings.
2. **Checks GC Content:** Calculates the GC percentage for both sequences. I included this because checking GC content is a vital metric for things like PCR primer stability in the lab.
3. **Finds the Mutation:** Runs a pairwise alignment to map the two sequences. The output visually flags the exact base-pair mismatch (the SNP) using a `.`.

## Next Steps
This project is part of my ongoing transition into computational biology. My next goal for this script is to scale it up so it can read and align bulk `.fasta` files instead of just short strings!
