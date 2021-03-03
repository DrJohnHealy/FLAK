<img src="images/logo.png" alt="Flak 1.0 - Ultra-fast Fuzzy Whole-genome Alignment" width="800" height="100" border="0"/>

<h1>Overview</h1>
FLAK (Fuzzy Logic Analysis of k-mers) is a software system designed to perform a fast approximate whole-genome comparison of two DNA sequences and enable fuzzy operations to be performed on a finished alignment in a visual and intuitive way. In contrast with existing genome alignment systems that are based on exact-matching suffix tree data structures or provide approximations using the BLAST-like seed-and-extend model, FLAK has a built-in native mechanism for approximate sequence matching. The kernel of the FLAK system is an optimised fuzzy hash map that enables a genome to be searched in average O(1) running time. FLAK is written in Java and uses a 2-bit encoding mechanism to represent and compress each 32-mer substring of a genome into a single 64-bit (8 byte) primitive type. The representation of DNA sequence information as a bit vector greatly reduces the space complexity of the system and enables FLAK to scale from small prokaryotic genomes (<5Mbps) to large mammalian chromosomes or genomes (>3 Gbps). Moreover, the exploitation of bit vectors using low-level binary shift operations further reduces the time complexity of genome alignment.

<p/>
<img src="images/screen.png" width="800" height="639" border="0">
<p/>


<h2>Why Use FLAK?</h2>
Because FLAK asks a different kind of question. FLAK alignments are based on fuzzy logic and fuzzy sets and can accommodate vagueness. In the context of biological sequence alignment, the vagueness in question relates to the degree of homology between two sequences. As FLAK is designed around fuzzy sets and fuzzy logic, the alignment system is fundamentally different to all existing genome aligners and deals with degrees of fuzzy set membership and degrees of homology. All existing whole-genome aligners are based on bivalent boolean logic and, at an abstract level, ask the question "Are the sequences homologous?". In contrast, the fuzzy nature of FLAK is designed to answer the question "how homologous are the sequences?". Re-formulating the alignment problem in this manner enables users of FLAK to perform analyses not possible using conventional models.
 

<h2>What You See is What You Get</h2>
FLAK is designed to be a simple, graphical, wizard-based system for configuring, executing and analysing a whole-genome alignment. From a usability perspective, the software allows for the what-you-see-is-what-you-get (WYSIWYG) viewing and extraction of alignment information using a toolbar of fuzzy options and filters. Users can employ a wizard to customise alignment parameters and may filter or modify the visualisation of an alignment using a range of GUI options.

