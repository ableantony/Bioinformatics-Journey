# Day 05: Proteins: From Gene to Function

**Date:** 23/10/2026
**Topic:** Biology only (no Linux, no coding)
**Follows:** Day 1 (central dogma) and Day 4 (genes, genome, mutations)

---

## 1. Where proteins fit

- Central dogma: DNA → RNA → **protein**.
- A gene is a recipe; the protein is the finished product that does the work.
- Proteins build structures, speed up reactions, carry signals, transport molecules, defend the body and regulate genes.
- In bioinformatics, a huge share of the data we analyze is protein sequences and structures.

---

## 2. Amino acids: the building blocks

- A protein is a chain of **amino acids** joined by **peptide bonds**.
- There are **20 standard amino acids**.
- Every amino acid has the same backbone: a central carbon (Cα) bonded to
  - an **amino group** (–NH₂)
  - a **carboxyl group** (–COOH)
  - a hydrogen
  - a variable **R group (side chain)**
- The R group decides the amino acid's chemistry.

### Groups by side chain

| Group | Examples | Behaviour |
|---|---|---|
| Nonpolar (hydrophobic) | Ala, Val, Leu, Ile, Met, Phe, Trp, Pro | Avoid water, usually buried inside the protein |
| Polar uncharged | Ser, Thr, Cys, Asn, Gln, Tyr | Like water, form hydrogen bonds |
| Positively charged (basic) | Lys, Arg, His | Attract negative charges |
| Negatively charged (acidic) | Asp, Glu | Attract positive charges |

- Glycine: smallest side chain (just H), very flexible.
- Proline: ring structure, creates kinks in the chain.
- Cysteine: can form **disulfide bonds** (S–S) with another cysteine.

### One-letter codes (used in FASTA files)
A Ala, R Arg, N Asn, D Asp, C Cys, Q Gln, E Glu, G Gly, H His, I Ile, L Leu, K Lys, M Met, F Phe, P Pro, S Ser, T Thr, W Trp, Y Tyr, V Val.

---

## 3. From codons to a protein (quick link to Day 1)

- mRNA is read in **codons** (3 nucleotides = 1 amino acid).
- **AUG** = start codon (Met). **UAA, UAG, UGA** = stop codons.
- Translation happens on the **ribosome**; **tRNA** brings the right amino acid for each codon.
- The chain grows from the **N-terminus** (amino end) to the **C-terminus** (carboxyl end).
- The genetic code is **redundant** (61 codons for 20 amino acids), so some DNA changes do not change the protein.

---

## 4. Four levels of protein structure

1. **Primary:** the amino acid sequence itself (N → C). Everything else follows from it.
2. **Secondary:** local folding held by hydrogen bonds in the backbone.
   - **α-helix:** coiled spiral.
   - **β-sheet:** strands lying side by side (parallel or antiparallel).
   - Loops/turns connect them.
3. **Tertiary:** the full 3D shape of one chain, held by
   - hydrophobic packing (the main driver)
   - hydrogen bonds
   - ionic bonds (salt bridges)
   - disulfide bonds
4. **Quaternary:** several chains (subunits) assembled together. Example: **hemoglobin** has 4 subunits.

- A distinct, independently folding region of a protein is called a **domain**. Many proteins are made of several domains.
- A short recurring pattern linked to function is called a **motif**.

---

## 5. Protein folding

- **Anfinsen's principle:** the sequence contains the information needed to fold into the correct 3D shape.
- Folding is driven by burying hydrophobic residues away from water.
- **Chaperones** help other proteins fold correctly and prevent clumping.
- **Denaturation:** heat, extreme pH or chemicals unfold a protein and it loses function (like an egg white turning solid when cooked).
- **Misfolding** can make proteins non-functional or toxic.

---

## 6. Structure decides function

- Shape creates **binding sites** where other molecules fit (lock and key / induced fit).
- **Enzymes:** protein catalysts that lower the activation energy of reactions.
  - **Active site:** the pocket where the **substrate** binds.
  - Affected by temperature, pH and inhibitors.
- Other protein roles:
  - Structural: collagen, keratin
  - Transport: hemoglobin
  - Defense: antibodies
  - Signaling: hormones, receptors
  - Movement: actin, myosin
  - Regulation: transcription factors
- Proteins are modified after translation (**post-translational modifications**), such as phosphorylation, glycosylation and cleavage, which switch activity on or off.

---

## 7. Mutations meet proteins (link to Day 4)

| Mutation type | Effect on protein |
|---|---|
| Silent | Codon changes, same amino acid, no change |
| Missense | Different amino acid, effect ranges from none to severe |
| Nonsense | Codon becomes a stop, protein cut short |
| Frameshift (insertion/deletion not a multiple of 3) | Reading frame shifts, protein usually ruined |

- **Sickle cell disease:** one missense change (Glu → Val) in the hemoglobin β chain makes hemoglobin clump, bending red blood cells.
- **Cystic fibrosis:** often caused by loss of one amino acid in the CFTR protein, causing misfolding.
- Conserved amino acids (unchanged across species) are usually the important ones, so changes there are more likely harmful.

---

## 8. Why this matters for disease and drug discovery

- Most drugs work by binding a **protein target** (enzyme, receptor, transporter) and changing its activity.
- Knowing the 3D structure of a target lets scientists design molecules that fit its binding site.
- Many diseases come from altered, missing or misfolded proteins.
- Microbes have their own proteins (e.g., bacterial enzymes) that antibiotics can target without harming human cells.

---

## 9. Bioinformatics connection (preview only)

- Sequence → structure → function is the core idea.
- Similar sequences often mean similar structure and function (the basis of sequence comparison, coming later).
- Key protein resources to meet later:
  - **UniProt:** protein sequences and functional information
  - **PDB (Protein Data Bank):** experimentally solved 3D structures
  - **AlphaFold DB:** predicted structures
  - **Pfam / InterPro:** domains and families

---

## 10. Key terms

- **Amino acid:** monomer of proteins.
- **Peptide bond:** covalent link between amino acids.
- **Polypeptide:** a chain of amino acids.
- **Residue:** an amino acid inside a chain.
- **R group:** variable side chain.
- **N-terminus / C-terminus:** the two ends of a chain.
- **Domain / motif:** structural region / short functional pattern.
- **Active site:** enzyme's substrate-binding pocket.
- **Chaperone:** helper that assists folding.
- **Denaturation:** loss of 3D structure.
- **Post-translational modification:** chemical change after translation.

---

## 11. Quick recap

- Gene → mRNA → chain of amino acids → folded protein.
- 20 amino acids; the R group gives each its character.
- Four structure levels: primary, secondary, tertiary, quaternary.
- Sequence determines the fold, and the fold determines function.
- Mutations can change the sequence and so the protein's shape and job.
- Proteins are the main targets of drugs.
