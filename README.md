# Viral Variant Calling
A Bash script for variant calling using BWA-MEM and SAMtools on a cluster such as Alabama Super Computer (ASC) with the assumption that these tools have been already installed. The pipeline takes raw sequencing data in FASTQ format and a reference genome in FASTA format, and outputs variant calls in VCF format.

## Prerequisites
Before running the script, you should make sure that the following modules are loaded on the remote cluster:

- Trimmomatic
- SPAdes
- BWA
- SAMtools
- BCFtools

The availability of the module on your cluster can be checked by 
<p><code>module avail &lt;tool_name&gt;</code></p>

## Input

The pipeline requires two inputs:
1. Directory containing the raw sequencing files
2. Path to the reference genome file (in fasta format)

## Usage
To run the pipeline, use the following command:

<p><code>./Viral_Variant_Call.sh</code></p>

The program will prompt for the name/path to the raw FASTQ files directory and the reference genome
## Output
The pipeline outputs sample_wise files into the following directories:

1. final_bam_files: Directory containing the final sorted BAM files.
2. contigs_files: Directory containing the assembled contigs.
3. assembly_stats_files: Directory containing assembly statistics files.
4. sam_files: Directory containing the SAM files.
5. vcf_files: Directory containing the VCF files for each sample.

## References
The pipeline uses the following tools:
<ul>
    <li>Trimmomatic: <a href="http://www.usadellab.org/cms/?page=trimmomatic">http://www.usadellab.org/cms/?page=trimmomatic</a></li>
    <li>SPAdes: <a href="https://cab.spbu.ru/software/spades/">https://cab.spbu.ru/software/spades/</a></li>
    <li>BWA-MEM: <a href="https://github.com/lh3/bwa-mem">https://github.com/lh3/bwa-mem</a></li>
    <li>SAMtools: <a href="http://www.htslib.org/doc/samtools.html">http://www.htslib.org/doc/samtools.html</a></li>
    <li>Varscan: <a href="http://varscan.sourceforge.net/">http://varscan.sourceforge.net/</a></li>
</ul>






