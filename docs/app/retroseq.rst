.. _RetroSeq:

RetroSeq
=======================

简介
---------------

RetroSeq is a tool for discovery and genotyping of transposable element variants (TEVs) (also
known as mobile element insertions) from next-gen sequencing reads aligned to a reference genome
in BAM format. The goal is to call TEVs that are not present in the reference genome but present
in the sample that has been sequenced. It should be noted that RetroSeq can be used to locate any
class of  viral  insertion  in any  species where  whole-genome  sequencing data with a suitable
reference genome is available.

完整步骤
----------------

.. code:: bash

   module load miniconda3
   conda create -n mypy_py27 python=2.7
   source activate mypy_py27
   conda install -c hcc retroseq
