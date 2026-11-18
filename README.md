# Nucleotide-finder
To find out number of purines and pyrimidines in DNA sequences
# DNA sequence analyzer

sequence = input("Enter a DNA sequence: ATGCCCTAA").strip().upper()

# Remove whitespace and check for invalid characters
sequence = "".join(sequence.split())
valid_bases = set("ATCG")
invalid_bases = set(sequence) - valid_bases

if invalid_bases:
    print("Invalid DNA bases:", ", ".join(sorted(invalid_bases)))
else:
    print("\nDNA Sequence:", sequence)
    print("Length:", len(sequence))
    print("Adenine (A):", sequence.count("A"))
    print("Thymine (T):", sequence.count("T"))
    print("Cytosine (C):", sequence.count("C"))
    print("Guanine (G):", sequence.count("G"))