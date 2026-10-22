# Day 4 - 22/10/2026

## Topic: Genes, Genome and Mutations

### Gene
- A gene is a stretch of DNA that holds the instructions for making a functional product, usually a protein (some genes make functional RNA instead).
- Flow of information: DNA -> (transcription) -> mRNA -> (translation) -> protein.
- Every 3 bases of mRNA form a codon, and each codon codes for one amino acid (or a start/stop signal).

### Genome
- The genome is the complete set of DNA in an organism, including genes and the non-coding regions between them.
- The human genome has about 3 billion base pairs and roughly 20,000 protein-coding genes. Most of the genome is non-coding.
- Gene vs genome: a gene is one instruction, and the genome is the whole instruction book.
- Bacteria have much smaller genomes (a few million base pairs), which is why microbial genomes are good beginner data in bioinformatics.

### Mutation
- A mutation is a change in the DNA sequence.
- Types:
  - Point mutation (substitution): one base is changed for another.
  - Insertion: extra base(s) added.
  - Deletion: base(s) removed.
- Effects of a point mutation on the protein:
  - Silent: the codon changes but the amino acid stays the same.
  - Missense: the amino acid changes.
  - Nonsense: the codon becomes a stop codon, so the protein is cut short.
- Insertions or deletions that are not multiples of 3 cause a frameshift, which changes every codon after that point.

### Example: sickle cell disease
- Gene: HBB (makes beta-globin, part of hemoglobin).
- Mutation: a single base change A -> T in the codon for amino acid 6 (GAG -> GTG).
- Result: glutamic acid is replaced by valine (a missense mutation).
- Effect: hemoglobin can clump together, red blood cells become sickle-shaped, and this causes the disease.
- Lesson: one letter out of billions can cause a disease.

### Why this matters for bioinformatics
- Comparing a patient's DNA sequence to a reference genome is how we find mutations (variant calling).
- This links to my interests: human disease and drug discovery.
