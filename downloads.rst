=========
Downloads
=========

Source Downloads
~~~~~~~~~~~~~~~~

+--------------+-----------------------------------------------+-------------+
| Latest development snapshots                                               |
+==============+===============================================+=============+
| Server/Agent | https://github.com/ossec/ossec-hids/releases                |
+--------------+-----------------------------------------------+-------------+
| Web UI       | https://github.com/ossec/ossec-wui/release                  |
+--------------+-----------------------------------------------+-------------+
| Docs         | https://github.com/ossec/ossec-docs                         |
+--------------+-----------------------------------------------+-------------+

+---------------------+-----------------------------------------------+--------------------------+------------+
| Latest Stable Release (2.8.3)                                                                  |            |
+=====================+===============================================+==========================+============+
| Server/Agent Unix   | `ossec-hids-2.8.3.tar.gz`_ – `Release Notes`_ | `Unix Checksum`_         |            |
+---------------------+-----------------------------------------------+--------------------------+------------+
| Agent Windows       | `ossec-agent-win32-2.8.3.exe`_                | `Win Checksum`_          |            |
+---------------------+-----------------------------------------------+--------------------------+------------+
| Virtual Appliance   | `ossec-vm-2.8.2.ova`_ – `README`_             | `VA Checksum`_           |            |
+---------------------+-----------------------------------------------+--------------------------+------------+

.. _ossec-hids-2.8.3.tar.gz: https://bintray.com/artifact/download/ossec/ossec-hids/ossec-hids-2.8.3.tar.gz
.. _Release Notes: https://bintray.com/ossec/ossec-hids/ossec-hids/view#release
.. _Unix Checksum: https://bintray.com/artifact/download/ossec/ossec-hids/ossec-hids-2.8.3.tar.gz.sha256
.. _ossec-agent-win32-2.8.3.exe: https://bintray.com/artifact/download/ossec/ossec-hids/ossec-agent-win32-2.8.3.exe
.. _Win Checksum: https://bintray.com/artifact/download/ossec/ossec-hids/ossec-agent-win32-2.8.3.exe.sha256
.. _ossec-vm-2.8.2.ova: http://ossec.wazuh.com/vm/ossec-vm-2.8.2.ova
.. _README: http://ossec.wazuh.com/vm/ossec-vm-2.8.2.README
.. _VA Checksum: http://ossec.wazuh.com/vm/ossec-vm-2.8.2-checksum.txt

RPMs for RHEL, CentOS, Fedora and others
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Available in the `Atomicorp repository <http://www5.atomicorp.com/channels/ossec/>`_.

+------------------------------------------------------------------------------------------------+
| CentOS                                                                                         |
+==============+=================================================================================+
| el5          | `i386 <http://www5.atomicorp.com/channels/ossec/centos/5/i386/RPMS/>`_          |
+--------------+---------------------------------------------------------------------------------+
| el5          | `x86_64 <http://www5.atomicorp.com/channels/ossec/centos/5/x86_64/RPMS/>`_      |
+--------------+---------------------------------------------------------------------------------+
| el6          | `i386 <http://www5.atomicorp.com/channels/ossec/centos/5/i386/RPMS/>`_          |
+--------------+---------------------------------------------------------------------------------+
| el6          | `x86_64 <http://www5.atomicorp.com/channels/ossec/centos/6/x86_64/RPMS/>`_      |
+--------------+---------------------------------------------------------------------------------+

+------------------------------------------------------------------------------------------------+
| Fedora                                                                                         |
+==============+=================================================================================+
| el5          | `i386 <http://www5.atomicorp.com/channels/ossec/fedora/20/i386/RPMS/>`_         |
+--------------+---------------------------------------------------------------------------------+
| el5          | `x86_64 <http://www5.atomicorp.com/channels/ossec/fedora/5/x86_64/RPMS/>`_      |
+--------------+---------------------------------------------------------------------------------+
| el6          | `i386 <http://www5.atomicorp.com/channels/ossec/fedora/5/i386/RPMS/>`_          |
+--------------+---------------------------------------------------------------------------------+
| el6          | `x86_64 <http://www5.atomicorp.com/channels/ossec/fedora/6/x86_64/RPMS/>`_      |
+--------------+---------------------------------------------------------------------------------+
| All          | `6 - 20 <http://www5.atomicorp.com/channels/ossec/fedora/>`_                    |
+--------------+---------------------------------------------------------------------------------+

RPM Installation
================

To install with yum do the following:

.. code:: console

    # wget -q -O – https://www.atomicorp.com/installers/atomic | sh
    # yum install ossec-hids ossec-hids-server (or ossec-hids-client for the agent)


DEBs for Debian and Ubuntu
~~~~~~~~~~~~~~~~~~~~~~~~~~

Available in the `Wazuh repository <http://ossec.wazuh.com/repos/apt/>`_.

+------------------+-----------------------------------------------------------------------------+
| Debian/Ubuntu                                                                                  |
+==================+=============================================================================+
| OSSEC Server     | `Debian`_, `Ubuntu`_                                                        |
+------------------+-----------------------------------------------------------------------------+
| OSSEC Agent      | `Debian`_, `Ubuntu`_                                                        |
+------------------+-----------------------------------------------------------------------------+

.. _Debian: http://ossec.wazuh.com/repos/apt/debian/pool/main/o/ossec-hids/
.. _Ubuntu: http://ossec.wazuh.com/repos/apt/ubuntu/pool/main/o/ossec-hids/

DEB Installation
================

To install with apt-get do the following:

Step 1. Install the apt-get repository key:

.. code:: console

    # apt-key adv --fetch-keys http://ossec.wazuh.com/repos/apt/conf/ossec-key.gpg.key

Step 2. Add the repository for Debian (available distributions are Sid, Jessie and Wheezy):

.. code:: console

    # echo ‘deb http://ossec.wazuh.com/repos/apt/debian wheezy main’ >> /etc/apt/sources.list

Or add the repository for Ubuntu (available distributions are Precise, Trusty and Utopic):

.. code:: console

    # echo ‘deb http://ossec.wazuh.com/repos/apt/ubuntu precise main’ >> /etc/apt/sources.list

Step 3. Update the repository:

.. code:: console

    # apt-get update

Step 4. Install OSSEC HIDS server/manager:

.. code:: console

    # apt-get install ossec-hids

Or install OSSEC HIDS agent:

.. code:: console

    # apt-get install ossec-hids-agent

PGP key
~~~~~~~

Before you install any package from our project, we recommend that you
verify it using our PGP key. Follow these two steps if you are not used
to using gpg. You first need to import our public key:

.. code:: console

    ossec-test# wget http://ossec.github.io/files/OSSEC-PGP-KEY.asc
    ossec-test# gpg –import OSSEC-PGP-KEY.asc

And then verify each file against its signature:

.. code:: console

    ossec-test# gpg –verify file.sig file

You should get the following result:


.. code:: console

    gpg: Signature made Tue 19 Jul 2011 03:13:58 PM BRT using RSA key ID A3901351
    gpg: Good signature from “Daniel B. Cid ”
    Primary key fingerprint: 6F11 9E06 487A AF17 C84C E48A 456B 17CF A390 1351

Note that the key expiration date was changed lately. If you get an
warning saying “gpg: Note: This key has expired!”, make sure to update
the key and run the “import” command again (as specified above).

Contribute back!
~~~~~~~~~~~~~~~~

If you find ossec useful and would like to contribute back to the
community, please contact us. We have a lot of work to do and any help
is appreciated.

|
