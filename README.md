# Python-Experiments GC Content 
from Bio.Seq import Seq
from Bio.SeqUtils import gc_fraction

def calculate_gc_content(sequence):

    seq_obj = Seq(sequence)  # Convert string to Biopython Seq object
    gc_content = gc_fraction(seq_obj) * 100  # Calculate GC fraction and convert to percentage
    return gc_content

dna_sequence = input("Input the DNA Sequence to calculate =" )
gc_content = calculate_gc_content(dna_sequence)
print(f"GC Content: {gc_content:.2f}%")
