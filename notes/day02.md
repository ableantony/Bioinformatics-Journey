# Day 2: DNA to Protein

## DNA
- Double helix, two antiparallel strands (5' to 3' and 3' to 5')
- Base pairs: A-T (2 H-bonds), G-C (3 H-bonds)
- Sequences in databases are written 5' to 3'
- Reverse complement of 5'-GATTACA-3' is 5'-TGTAATC-3'

## Replication
- Semi-conservative: each new helix has one old and one new strand
- Helicase unzips, primase adds primer, DNA polymerase extends 5' to 3' (and proofreads), ligase seals gaps
- Leading strand is continuous; lagging strand is made as Okazaki fragments

## Transcription (DNA to mRNA)
- RNA polymerase reads the template strand
- RNA uses U instead of T
- Humans: introns are spliced out, exons are kept. Bacteria mostly have no introns

## Translation (mRNA to protein)
- Ribosome reads codons (3 bases = 1 amino acid), tRNA brings amino acids
- Start codon: AUG (Met). Stop codons: UAA, UAG, UGA
- Code is redundant: 64 codons, 20 amino acids
- Example: AUG GCU UAC UAA = Met-Ala-Tyr-stop

## Mutations
| Type | Effect |
|---|---|
| Silent | Same amino acid, no change |
| Missense | Different amino acid |
| Nonsense | New stop codon, short protein |
| Frameshift | Insertion/deletion not in multiples of 3, changes every later codon |

- Sickle cell anemia: one missense change in the hemoglobin gene (Glu to Val)

## Why it matters for bioinformatics
Most tools work on these sequences: comparing them, finding genes, and spotting mutations.
