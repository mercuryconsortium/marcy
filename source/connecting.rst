*******************
Connecting to Marcy
*******************
In order to run jobs on Marcy, the user must gain command line access Marcy from a
personal/work computer using `Secure Shell protocol <https://www.ssh.com>`_ (SSH).
Connecting through SSH works differently on different operating systems, so instructions
for the two most common cases are presented below.

SSH on Mac OS X and UNIX
========================
Open a command line terminal application on your local computer (``localhost``) and
use the ``ssh`` command.
.. code-block:: bash

   localhost$ ssh username@marcy.furman.edu

SSH on Windows
==============
Windows users must use a secure shell client. `PuTTY <https://putty.org>`_ is the recommended
program for this task, so we will this program in the instructions below.

Download and install `PuTTY <https://putty.org>`_ on your local computer (``localhost``). Open
a new SSH connection and edit the prompt accordingly. Enter ``marcy.furman.edu`` in the 
`Host Name` box and click `Open`. A command line terminal will open and ask for your account
credentials. Enter your username and password to gain access to Marcy.

.. toctree::
   :maxdepth: 2
   :caption: Contents
