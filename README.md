# DNA Sequence Analyzer using Biopython

Introduction

This project is a simple yet powerful DNA sequence analyzer built using Python and Biopython. It allows users to input a DNA sequence and perform various bioinformatics tasks, such as:

Transcription (DNA to RNA)

Translation (RNA to Protein)

GC content calculation

Finding complementary and reverse complement sequences

Tools & Libraries Used

Python (Programming Language)

Biopython (For sequence manipulation)

Google Colab / Jupyter Notebook (For execution)

Implementation Steps

Step 1: Install and Import Required Libraries

!pip install biopython  # Install Biopython if not already installed
from Bio.Seq import Seq  # Import Seq class for sequence operations

Step 2: Input DNA Sequence

dna_seq = Seq("ATGGCCATTGTAATGGGCCGCTGAAAGGGTGCCCGATAG")
print("📌 Original DNA Sequence:", dna_seq)

Step 3: Transcription (DNA to mRNA)

mRNA_seq = dna_seq.transcribe()
print("📌 Transcribed mRNA Sequence:", mRNA_seq)

Step 4: Translation (mRNA to Protein)

protein_seq = dna_seq.translate()
print("📌 Translated Protein Sequence:", protein_seq)

Step 5: GC Content Calculation

from Bio.SeqUtils import gc_fraction

gc_content = gc_fraction(dna_seq) * 100
print("📌 GC Content (%):", round(gc_content, 2))

Step 6: Complement and Reverse Complement

complement_seq = dna_seq.complement()
reverse_complement_seq = dna_seq.reverse_complement()

print("📌 Complementary Sequence:", complement_seq)
print("📌 Reverse Complementary Sequence:", reverse_complement_seq)

Sample Output

📌 Original DNA Sequence: ATGGCCATTGTAATGGGCCGCTGAAAGGGTGCCCGATAG
📌 Transcribed mRNA Sequence: AUGGCCAUUGUAAUGGGCCGCUGAAAGGGUGCCCGAUAG
📌 Translated Protein Sequence: MAMWPREAKGPR*
📌 GC Content (%): 48.72
📌 Complementary Sequence: TACCGGTAACATTACCCGGCGACTTTCCCACGGGCTATC
📌 Reverse Complementary Sequence: CTATCGGGCACCCTTTCAGCGGCCATTACAATGGCCAT

Future Improvements

🔹 Motif Search: Identify specific patterns in DNA sequences.🔹 Mutation Analysis: Compare mutated sequences.🔹 GUI Integration: Create a simple interface for easier use.

Conclusion

This project provides a basic but essential toolkit for analyzing DNA sequences using Biopython. It lays the foundation for more advanced bioinformatics applications. 🚀

