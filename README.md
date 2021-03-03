<table bgcolor="#FFFFFF" width="100%" cellspacing="0" cellpadding="5" border="0">
		<tr>
			<td colspan="4" bgcolor="#6699cc">
				<img src="images/filler.png" alt="Flak 1.0 - Ultra-fast Fuzzy Whole-genome Alignment" width="800" height="40" border="0"/>
			</td>
		</tr>
		<tr>
			<td colspan="4">
				<a href="index.html"><img src="images/logo.png" alt="Flak 1.0 - Ultra-fast Fuzzy Whole-genome Alignment" width="800" height="100" border="0"/></a>&nbsp;&nbsp;
				<a class="largeButton" href="download.html">Download FLAK 1.0</a>
				<p/>
			</td>
		</tr>
		<tr>
			<td width="350" valign="top">				
  				<ul>
  					<li><a href="index.html">Overview</a></li>					
  					<li><a href="sysreq.html">System Requirements</a></li>
					<li><a href="download.html">Download FLAK</a></li>
					<li><a href="license.html">Software License</a></li>
					<li><a href="quick.html">Quick Start</a></li>
				    <li><a href="memory.html">Configuring Memory</a></li>
				    <li><a href="native.html">Native Approximate Sequence Alignment</b></li>
					<li><a href="seeds.html">Fuzzy Seeds</b></li>
				    <li><a href="custom.html">Creating Alignment Seeds</b></li>
				    <li><a href="overlaps.html">Custom Control of Reference Overlaps</b></li>
				    <li><a href="fuzzyops.html">Hedges & Fuzzy Operators</a>
				    <li><a href="vis.html">Alignment Visualisation</li>
				    <li><a href="filtering.html">Alignment Filtering</li>
		  			<li><a href="output.html">Alignment Output</a></li>
					<li><a href="benchmarks.html">Performance Benchmarks*</a></li>
					<li><a href="pubs.html">Publications</a></li>
				    <li><a href="contact.html">Contact Information</a></li>
  				</ul>
			</td>
      <td width="10" valign="top">&nbsp;</td>
			<td valign="top">
<!-Start of Main Body>

<h1>Overview</h1>
FLAK (<b>Fuzzy Logic Analysis of <i>k</i>-mers</b>) is a software system designed to perform a fast approximate whole-genome comparison of two DNA sequences and enable
fuzzy operations to be performed on a finished alignment in a visual and intuitive way. In contrast with existing genome alignment systems that are based
on exact-matching suffix tree data structures or provide approximations using the BLAST-like <i>seed-and-extend</i> model, FLAK has a built-in native mechanism for
approximate sequence matching. The kernel of the FLAK system is an optimised fuzzy hash map that enables a genome to be searched in average <i>O</i>(1)
running time. FLAK is written in Java and uses a 2-bit encoding mechanism to represent and compress each 32-mer substring of a genome into a single 64-bit
(8 byte) primitive type. The representation of DNA sequence information as a bit vector greatly reduces the space complexity of the system and enables
FLAK to scale from small prokaryotic genomes (&lt;5Mbps) to large mammalian chromosomes or genomes (&gt;3 Gbps). Moreover, the exploitation of bit vectors
using low-level binary shift operations further reduces the time complexity of genome alignment.
<p/>&nbsp;<p/>
<img src="images/screen.png" width="800" height="639" border="0">
<p/>&nbsp;<p/>




<h2>Why Use FLAK?</h2>
Because FLAK asks a different kind of question. FLAK alignments are based on fuzzy logic and fuzzy sets and can accommodate vagueness. In the context of biological sequence alignment, the vagueness in question relates to
the degree of homology between two sequences. As FLAK is designed around fuzzy sets and fuzzy logic, the alignment system is fundamentally different to
all existing genome aligners and deals with degrees of fuzzy set membership and degrees of homology. All existing whole-genome aligners are based on bivalent
boolean logic and, at an abstract level, ask the question <i>"Are the sequences homologous?"</i>. In contrast, the fuzzy nature of FLAK is designed to answer the
question <i>"how homologous are the sequences?"</i>. Re-formulating the alignment problem in this manner enables users of FLAK to perform analyses not possible using conventional models.
<p/>&nbsp;<p/>


<h2>What You See is What You Get</h2>
FLAK is designed to be a simple, graphical, wizard-based system for configuring, executing and analysing a whole-genome alignment. From a usability
perspective, the software allows for the what-you-see-is-what-you-get (WYSIWYG) viewing and extraction of alignment information using a toolbar of fuzzy options and
filters. Users can employ a wizard to customise alignment parameters and may filter or modify the visualisation of an alignment using a range of GUI options.
<p/>&nbsp;<p/>


<h2>Features</h2>

<ul>
	<li><span class="flak-emp">Ultra-Fast Whole-Genome Alignment:</span> The running times exhibited by FLAK out-perform all existing whole-genome aligners across a range of genome sizes and types, including large repeat-rich sequences. FLAK can align the genomes of E.<i>coli</i> K12 MG1655 (4.7Mbps) v E.<i>coli</i> 536 (5.0Mbps) in 2 seconds, H.<i>sapiens</i> Chromosome X (158.29Mbps) v M.<i>musculus</i> Chromosome X (169.27Mbps) in 169 seconds
and P.<i>abelii</i> Chromosome 1 (264.71Mbps) v H.<i>sapiens</i> Chromosome 1 (231.11Mbps) in 231 seconds.</li></p>
	<li><span class="flak-emp">Low Memory Requirements:</span> FLAK is designed to consume as little memory as possible and uses bit encoding and flyweights to reduce the space complexity of a large-scale alignment. As a result, FLAK can compare full primate genomes (&gt;3.2Gbps) on a computer with 16Gb of RAM.</li></p>

	<li><span class="flak-emp">Native Approximate Sequence Alignment:</span> FLAK supports native approximate <i>k</i>-mer matching and is capable of identifying approximate matches above a user defined threshold. This allows FLAK to provide a more detailed analysis of a genome alignment and identify putative homologous regions of genomes that existing approaches often miss.</li></p>

	<li><span class="flak-emp">Custom Alignment Seeds:</span> FLAK permits the parametrisation of an alignment with any type of seed with a length &le;32. This includes both consecutive seeds and spaced-seeds.</li></p> 

	<li><span class="flak-emp">Fuzzy Operators and Hedges:</span> FLAK enables the application of fuzzy operators to genome alignments. These include the basic fuzzy operators and a set of hedges to modify the fuzzy set of alignments. Once an alignment has been completed, these fuzzy logic operations can be applied to the alignment data in real time, with the system providing a visual representation of the modified data and also allowing the modified data to be saved in numeric or visual forms.</li></p>

	<li><span class="flak-emp">Alignment Visualisation:</span> FLAK provides users with a simple, graphical, wizard-based system for configuring, executing and analysing a whole-genome alignment. From a usability perspective, the software allows for WYSIWYG (What-You-See-Is-What-You-Get) viewing and extraction of alignment information using a toolbar of fuzzy options.</li></p>

	<li><span class="flak-emp">Alignment Filtering:</span> FLAK supports the <i>post hoc</i> filtering of alignments based on a minimum alignment length criterion. Filtered alignments are visualised and outputted, enabling users to visually experiment with a revocable filtering operation to search for extended areas of homology between two genomes.</li></p>

	<li><span class="flak-emp">Custom Control of Reference Overlaps:</span> By default, FLAK builds an alignment database from the set of contiguous non-overlapping 32-mers in a reference genome. To increase the sensitivity of comparison, users can specify a degree of overlap between the 32-mers extacted from the reference genome.</li></p>

</ul>
<p/>&nbsp;<p/>


<h2>What FLAK Doesn't Do...Yet</h2>
FLAK is designed to rapidly align two genomes and has been tested for robustness for this purpose only. The following activities and usage are currently not supported by FLAK, but will be available in future releases:
<ul>
	<li>Process protein sequences.</li>
	<li>Compare sequence reads against a genome.</li>
	<li>Compare contigs against a draft genome.</li>
</ul>
<p/>&nbsp;<p/>


<h1>Availability</h1>
FLAK is free for non-commercial use and can be downloaded from <a href="download.html">here</a>. Commercial users can purchase a license for FLAK from <a href="license.html">here</a>.

<!-End of Main Body>
<p/>&nbsp;<p/>
			</td>
			<td width="50">&nbsp;</td>
	</table>
