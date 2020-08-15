SSH on Mac OS X or Linux
========================
Open a `command line terminal <https://help.gnome.org/users/gnome-terminal/stable/>`_  on your local
computer (``localhost``) and use the ``ssh`` command. You will need your MERCURY account password for
this, unless you have set up passwordless access.

.. code-block:: bash

    username@localhost:~$ ssh username@marcy.furman.edu
    Last login: Fri Aug 14 21:43:34 2020 from 10.101.80.1
         +-+-+-+-+-+-+-+-+-+-+-+-+-++-+-+-+-+-+-+-+-+-+-+
         |    |M|A|R|C|Y| @       MERCURY Consortium    |
         +-+-+-+-+-+-+-++-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
    Ganglia - 	http://marcy.furman.edu/ganglia/
    WebMO - 	http://marcy.furman.edu/webmo.html	(mercuryuser:marcy)

    UPDATES:

    02/08/15 - NEW queue rules are implemented
    See http://marcy.furman.edu/wiki/doku.php/start?&#running_calculations for details
    If you submit to the 'mercury' queue requesting the necessary resources
    (walltime=x:x:x, nodes=x:ppn=x, mem=xGB), the job will be routed to the best queue.

    08/15/14 - Example runs and benchmarks are compiled at ~software_test
      or online at http://marcy.furman.edu/~software_test

    Send any support requests to support@mercuryconsortium.org
    [username@master ~]%

Passwordless SSH on Mac OS
--------------------------
The user's local SSH key must be installed on Marcy to allow passwordless SSH.

Checking for a Previous Key
"""""""""""""""""""""""""""
Open a command line terminal on your local computer (``localhost``) and list the home directory
contents including hidden files/folders.

.. code-block:: bash

   localhost$ ls -al

If the folder ``.ssh`` exists and contains the files ``id_rsa`` and ``id_rsa.pub`` a previously-generated
SSH key exists and can be used. If the folder ``.ssh`` does NOT exist, the user must generate a new
SSH key.

Generating a New Key
""""""""""""""""""""
Use the ``ssh-keygen`` command and accept the default configurations in the resulting prompts.

.. code-block:: bash

   localhost$ ssh-keygen

This will create the folder ``/Users/username/.ssh`` which contain the files ``id_rsa`` and ``id_rsa.pub``.

Installing Key on Marcy
"""""""""""""""""""""""
Change directory to the ``.ssh`` folder.

.. code-block:: bash

   localhost$ cd /Users/username/.ssh

Create a temporary ``authorized_keys`` file containing your public key.

.. code-block:: bash

   localhost$ cp id_rsa.pub temporary_authorized_keys

Transfer the temporary file to Marcy.

.. code-block:: bash

   localhost$ scp temporary_authorized_keys username@marcy.furman.edu:/home/username/.ssh/authorized_keys

This completes the SSH key installation and allows passwordless SSH and SCP.


.. toctree::
   :maxdepth: 4
   :caption: Contents
