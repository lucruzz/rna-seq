# RNA-seq Scientific Workflow
Workflow for RNA sequencing using the Parallel Scripting Library - Parsl.

## Requirements

In order to use RNA-seq Workflow the following tools must be available:

- [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)

You can install Bowtie2 by running:

```sh
bowtie2-2.3.5.1-linux-x86_64.zip
```

Or

```sh
sudo yum install bowtie2-2.3.5-linux-x86_64
```

- [HTSeq](https://htseq.readthedocs.io/en/master/)

HTSeq is a native Python library that folows conventions of many Python packages. You can install it by running:

```sh
pip install HTSeq
```

HTSeq uses [NumPy](https://numpy.org/), [Pysam](https://github.com/pysam-developers/pysam) and [matplotlib](https://matplotlib.org/). Be sure this tools are installed.

- [R](https://www.r-project.org/)

To use [DESEq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html) script make sure R language is also installed. You can install it by running:

```sh
sudo apt install r-base
```

- [Parsl - Parallel Scripting Library](https://parsl.readthedocs.io/en/stable/index.html)

The recommended way to install Parsl is the suggest approach from Parsl's documantion:

```sh
python3 -m pip install parsl
```

- [Python (version >= 3.5)](https://www.python.org/)

To use Parsl, you need Python 3.5 or above. You also need Python to use HTSeq, so you should load only one Python version.

## Workflow invocation

First of all, make a Comma Separated Values (CSV) file. So, onto the first line type: ``sampleName,fileName,condition``. **Remember, there must be no spaces between items**. You can use the table.csv file in this repository as an example.

| sampleName | fileName | condition |
|---|---|---|
|   |   |   |
|   |   |   |
|   |   |   |

On this first version the workflow search, on the input files' directory, for a pattern on the prefix in the files' name. So, for running this workflow you need pass this pattern.
