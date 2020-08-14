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
Marcy has 26 compute nodes grouped into queues based on their hardware configuration. Users
connect to Marcy by logging into the login node via `SSH <https://www.ssh.com>`_. Jobs
are submitted from the login node via `PBS <https://www.openpbs.org>`_ to the compute nodes.
The cluster's file system is located on the storage node in a large RAID array of hard
disks.

Login Node
----------
Users connect to Marcy by logging into the login node using `SSH <https://www.ssh.org>`_. This
interactive session runs on the `TCSH <https://www.tcsh.org>`_ shell.

  ===================== ================================
  master                master
  ===================== ================================
  Processor             Intel Broadwell E5-2660 2.20 GHz
  Number of processors  2
  Threads per processor 8
  Threads per node      16
  Memory per processor  4 GB
  Memory per node       64 GB
  Disk space per node   2 TB
  ===================== ================================

Storage Node
------------
Marcy's file system is stored in a 27 TB `RAID <https://en.wikipedia.org/wiki/RAID>`_ array of
hard disks on the storage node. This is where long-term storage of data is located. The file
system is backed up weekly.

  ===================== ================================
  io                    io
  ===================== ================================
  Processor             Intel Broadwell E5-2660 2.20 GHz
  Number of processors  2
  Threads per processor 8
  Threads per node      16
  Memory per processor  4 GB
  Memory per node       64 GB
  Disk space per node   20 TB
  ===================== ================================

Compute Nodes
-------------
Jobs submitted to the queue from the ``master`` node are sent to the proper compute nodes
depending on the requested resources. Jobs with light, moderate, and heavy memory requirements
are sent to the ``smallmem``, ``mediummem``, and ``bigmem`` nodes to carry out their
calculations. Jobs running `CUDA <https://developer.nvidia.com/about-cuda>`_ code are sent to
the ``gpu`` node.

  ===================== ================================
  smallmem              inode[9-21]
  ===================== ================================
  Processor             Intel Broadwell E5-2660 2.20 GHz
  Number of processors  2
  Threads per processor 8
  Threads per node      16
  Memory per processor  2 GB
  Memory per node       32 GB
  Disk space per node   1 TB
  ===================== ================================


  ===================== ================================
  mediummem             inode[21,23-26]
  ===================== ================================
  Processor             Intel Broadwell E5-2660 2.20 GHz
  Number of processors  2
  Threads per processor 8
  Threads per node      16
  Memory per processor  4 GB
  Memory per node       64 GB
  Disk space per node   1 TB
  ===================== ================================


  ===================== ================================
  bigmem                inode[1-8]
  ===================== ================================
  Processor             Intel Broadwell E5-2660 2.20 GHz
  Number of processors  2
  Threads per processor 8
  Threads per node      16
  Memory per processor  8 GB
  Memory per node       128 GB
  Disk space per node   2 TB
  ===================== ================================


  ===================== ================================
  gpu                   inode[22]
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
