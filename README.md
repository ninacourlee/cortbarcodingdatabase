**CORTINARIUS BARCODING DATABASE OF WESTERN SIBERIA AND ADJACENT AREAS - DATA ANALYSIS**

Bioinformatics Pipeline for Cortinarius Sequence Processing

1. Quality Control & Assembly

Raw sequences were filtered (Q ≥ 20 average, ≥15 ends, 50 bp min length) using a 5 bp sliding window.

Reads were trimmed at low-quality regions and assembled via Needleman-Wunsch alignment (match=2, mismatch=-3, gap_open=-5, gap_extend=-2). Contigs required ≥20 bp overlap, with forward-read priority for conflicts.

Sequence quality was scored as: (length × 0.4) - (%N × 0.6), categorized into: Failed/Low/Medium/Good/Excellent.

2. Taxonomic Assignment

Processed with massBLASTer (BLAST+ 2.13.0) against UNITE/INCB databases (PlutoF platform, 'Similar sequences (fast)' mode).

Best-hit selection criteria:

Strict species-level matches only (excluded sp./cf./aff.).

Priority to type specimens (is_type=True), then highest BLAST score.

Output includes: Taxon (best match), other_taxa (alternatives), and alignment metrics (identity/coverage).

3. Data Submission & Novelty Flagging

Sequences with 76-95% similarity assigned to genus level; 95-97% marked as aff. to flag potential new taxa.

Annotated tables include: raw sequences, filtered hits, and alignment stats for reproducibility.


**About the project**

Filippova N, Bulyonkova T, Zvyagina E, Ageev D. (2025). Cortinarius barcoding database of Western Siberia and adjacent areas. Biodiversity data journal. [in press]

**How to use the script**

Download processed metadata (sequences.csv) from /data folder in this repository
Download raw sequence (fastq.gz) arcive from ENA portal /link/
Load and run Jupyter Notebook (analysis.ipynb) for Google Colab
Generated Figures (PNG/PDF), statistical tables (CSV) are available in /output folder in this repository

**Data storage**

Note: Data updates will only occur via GBIF, GenBank and ENA repositories

(to be added) GenBank proejct
(to be added) GBIF dataset
(to be added) ENA archive


