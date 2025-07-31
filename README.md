# insilico-digestion-pyopenms

This repository provides a Python script for **in-silico enzymatic digestion** of protein sequences from a FASTA file/CSV file with Protien IDs using the [PyOpenMS](https://pyopenms.readthedocs.io/en/latest/) library. It simulates trypsin digestion, applies variable modifications (e.g., oxidation on methionine), and generates a CSV file with peptide sequences and molecular formulas. This Output can be used as a peptide library in Metaboscape.

## Prerequisites (Libraries to be installed)

- Python 3.7+
- PyOpenMS
- pandas

# FILE INPUT

# For FASTA input 
File Directory should be correct. In the default code input files should locate in the root directory.
fasta_file = "mcherry.fasta" # Replace mcherry.fasta with your FASTA file name
output_csv = "mcherr76y.csv" # Replace the required name of the output file with .csv extension

# For proteoscape input (CSV)

File Directory should be correct. In the default code input files should locate in the root directory.
input_csv = "1.csv" # Replace 1.csv with your CSV file name
file output_prefix = "metaboscape_peptides_part"  # No file extension required 


⚙️ DIGESTION PARAMETERS (IMPORTANT)
These parameters must be reviewed and adjusted as per your experiment:

ENZYME: Default is Trypsin (used by ProteaseDigestion() internally).

MISSED CLEAVAGES: 1
digestion.setMissedCleavages(1)

PEPTIDE LENGTH RANGE: Minimum = 6, Maximum = 40
min_length = 6
max_length = 40

VARIABLE MODIFICATIONS: Oxidation on Methionine

variable_mod_names = [b"Oxidation (M)"]
You can customize modification types (Refer to PyOpenMs Website https://pyopenms.readthedocs.io/en/latest/user_guide/peptides_proteins.html).

# How to run the script

Run the script using the terminal

python script.py

