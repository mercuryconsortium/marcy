SSH on Mac OS X or Linux
========================
Open a `command line terminal <https://help.gnome.org/users/gnome-terminal/stable/>`_  on your local
computer (``localhost``) and use the ``ssh`` command.

.. code-block:: bash
   
   localhost$ ssh username@marcy.furman.edu

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
