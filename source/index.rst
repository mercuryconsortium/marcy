.. Marcy User Guide documentation master file, created by
   sphinx-quickstart on Fri Aug 14 13:03:21 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

================
Marcy User Guide
================

Introduction
============
Marcy is one of the `Molecular Education and Research Consortium in Undergraduate Computational
Chemistry <https://mercuryconsortium.org>`_ high-performance computing clusters (HPCs).

System Overview
===============
Marcy has 26 compute nodes grouped into the following queues based on the hardware configuration.

.. table:: Login Node
   :caption: master

   ===================== ================================
   Processors            Intel Broadwell E5-2660 2.20 GHz
   Number of processors  2
   Threads per processor 8
   Threads per node      16
   Memory per processor  4 GB
   Memory per node       64 GB
   Disk space per node   2 TB
   ===================== ================================

.. table:: Storage Node
   :caption: io

   ===================== ================================
   Processors            Intel Broadwell E5-2660 2.20 GHz
   Number of processors  2
   Threads per processor 8
   Threads per node      16
   Memory per processor  4 GB
   Memory per node       64 GB
   Disk space per node   20 TB
   ===================== ================================

.. table:: Thin Nodes
   :caption: inode[9-20]

   ===================== ================================
   Processors            Intel Broadwell E5-2660 2.20 GHz
   Number of processors  2
   Threads per processor 8
   Threads per node      16
   Memory per processor  2 GB
   Memory per node       32 GB
   Disk space per node   1 TB
   ===================== ================================

.. table:: Medium Nodes
   :caption: inode[21,23-26]

   ===================== ================================
   Processors            Intel Broadwell E5-2660 2.20 GHz
   Number of processors  2
   Threads per processor 8
   Threads per node      16
   Memory per processor  4 GB
   Memory per node       64 GB
   Disk space per node   1 TB
   ===================== ================================

Big Nodes
---------
.. table:: Big Nodes
   :caption: inode[1-8]

   ===================== ================================
   Processors            Intel Broadwell E5-2660 2.20 GHz
   Number of processors  2
   Threads per processor 8
   Threads per node      16
   Memory per processor  8 GB
   Memory per node       128 GB
   Disk space per node   2 TB
   ===================== ================================

GPU Node
--------
.. table:: GPU Node
   :caption: inode[22]

   ===================== ================================
   Processors            Intel Broadwell E5-2660 2.20 GHz
   Number of processors  2
   Threads per processor 8
   Threads per node      16
   Memory per processor  2 GB
   Memory per node       32 GB
   Disk space per node   1 TB
   Graphics cards        NVIDIA Tesla K20
   Number of CUDA cores  2496
   ===================== ================================


.. toctree::
   :maxdepth: 2
   :caption: Contents

   system-overview
