# DNA Sequence Analysis Toolkit

This toolkit provides a series of functions for analyzing DNA sequences to identify codon patterns, open reading frames (ORFs), and the longest ORF within a sequence.

## Overview

The project is divided into the following steps:

1. **Finding all start codons**: Locate all occurrences of the `ATG` start codon.
2. **Finding in-register stop codons**: Identify the first stop codon (`TGA`, `TAG`, or `TAA`) in-frame.
3. **Identifying all ORFs**: Determine the ranges of all open reading frames in the sequence.
4. **Finding the longest ORF**: Extract the longest open reading frame from the sequence.

---

## Steps and Implementation Details

### Step 1: Implementing the `find_all_starts` Function
This function scans a DNA sequence and identifies all starting positions of the `ATG` codon.

- **Input**: A DNA sequence string (e.g., `"ATGCGTATGACG..."`).
- **Output**: A list of integers representing the indices of all `ATG` codons. If no `ATG` codons are found, an empty list is returned.

#### Example:
```python
find_all_starts("ATGCGTATGACG")
# Output: [0, 6]
