# MinION_Dummy
Dummy Pipeline

## Tasks according to project description

QC based on fastq

1. (fastq_utils)
2. guppy for demux
3. NanoPlot
4. nanoq
5. length filter
6. taxonom. classification (Kraken)
7. include results in MultiQC for reporting

## Tools

Potential tooling for the Pipeline

### Available via nf-core modules

- [Minimap2](https://github.com/nf-core/modules/tree/master/modules/minimap2) - read mapper
- [Kraken2](https://github.com/nf-core/modules/tree/master/modules/kraken2/kraken2) - tax. classification ([comparison paper](https://www.biorxiv.org/content/10.1101/2020.11.25.397729v2))
- [NanoPlot](https://github.com/nf-core/modules/tree/master/modules/nanoplot) - "fastqc for nanopore"
- [MultiQC](https://github.com/nf-core/modules/tree/master/modules/multiqc) - evaluation/reporting workflow
- [nanoseq](https://github.com/nf-core/nanoseq) - workflow including most of the above tools and functionality requirements
- [pycoQC](https://github.com/nf-core/modules/tree/master/modules/pycoqc) - computes metrics and generates QC plots for nanopore data
- [Filtlong](https://github.com/nf-core/modules/tree/master/modules/filtlong) - filtering long reads by quality

### Not available via nf-core modules

- [fastq_utils](https://github.com/nunofonseca/fastq_utils) - check file integrity
- [Nanoq](https://github.com/esteinig/nanoq) - fastq statistics and filter options after base calling
- [minion_qc](https://github.com/roblanf/minion_qc)
- [Guppy](https://nanoporetech.com) - base calling and demultiplexing, not freely available

## Roadmap

- write recipes for tooling that is not available via nf-core
  - [ ] fastq_utils
  - [ ] Nanoq
  - [ ] minion_qc
  - [ ] Guppy - probably not possible without access, shouldn't be a problem 
- implement minimal QC workflow, that is compatible with nf-core
- CI/Build (?)


