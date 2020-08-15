SSH on Mac OS X or Linux
========================
Open a `command line terminal <https://help.gnome.org/users/gnome-terminal/stable/>`_  on your local
computer (``localhost``) and use the ``ssh`` command. You will need your MERCURY account password for
this, unless you have set up passwordless access.

.. code-block:: bash

    username@localhost:~$ ssh username@marcy.furman.edu

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
Use the ``ssh-keygen`` command and accept the default configurations in the resulting prompts. This will create the folder ``/Users/username/.ssh`` which contain the files ``id_rsa`` and ``id_rsa.pub``.

.. code-block:: bash

    username@localhost:~$ ssh-keygen
    Generating public/private rsa key pair.
    Enter file in which to save the key (/Users/username/.ssh/id_rsa):
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    Your identification has been saved in /Users/username/.ssh/id_rsa.
    Your public key has been saved in /Users/username/.ssh/id_rsa.pub.
    The key fingerprint is:
    SHA256:72Qj8wd6hGnDGYMB8/YYPLIPm/dC1mP7B5xv27wRjds username@localhost.local
    The key's randomart image is:
    +---[RSA 2048]----+
    |    o.           |
    |     +.          |
    |    . *o         |
    |     +.=o      o |
    |    o .oSB .  o .|
    |     =o @.*    + |
    |    ooooo*=+  o E|
    |     ...oB..=o . |
    |       ..o++..+. |
    +----[SHA256]-----+
    username@localhost:~$ ls .ssh
    id_rsa		id_rsa.pub	known_hosts

Installing Key on Marcy
"""""""""""""""""""""""
Change directory to the ``.ssh`` folder and copy the public key file ``id_rsa.pub`` to a new file
called ``authorized_keys``. Then use ``scp`` to transfer the ``authorized_keys`` file to your
``.ssh`` folder on Marcy.

.. code-block:: bash

    username@localhost:~$ cd /Users/username/.ssh/
    username@localhost:~$ cp id_rsa.pub authorized_keys
    username@localhost:~$ scp authorized_keys username@marcy.furman.edu:/home/username/.ssh/.
    Password:
    authorized_keys                               100%  406    12.9KB/s   00:00

This completes the SSH key installation and allows passwordless SSH and SCP.


.. toctree::
   :maxdepth: 4
   :caption: Contents
