*******************
Connecting to Marcy
*******************
In order to run jobs on Marcy, the user must gain command line access Marcy from a
personal/work computer using `Secure Shell protocol <https://www.ssh.com>`_ (SSH).
Connecting through SSH works differently on different operating systems, so instructions
for the two most common cases are presented below.

SSH on Mac OS X and UNIX
========================
The most direct method is to connect directly from a command line terminal on a
Mac OS X or UNIX computer. This is because Marcy operates the CentOS 6 UNIX operating
system through a command line interface. Mac OS is built on UNIX, so has the command line
terminal software built in. So, user with the account ``username`` working from a personal
computer ``localhost`` can connect to Marcy using the command

.. code-block:: bash

   localhost$ ssh username@marcy.furman.edu

and entering their MERCURY HPC account password at the prompt.

.. toctree::
   :maxdepth: 2
   :caption: Contents
