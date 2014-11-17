=====================
RBTools Documentation
=====================

RBTools is a set of client tools to use with Review Board.


Using RBTools
=============

.. _rbt:

rbt
---

The recommended command-line interface is the :command:`rbt` tool. This tool
runs on Windows, Linux, and MacOS X, and allows executing a number of useful
sub-commands. :command:`rbt` has the following usage::

   $ rbt [--version] <command> [options] [<args>]

The :command:`rbt` command obsoletes the old "post-review" command.
For built in help you may execute::

   $ rbt help


.. toctree::
   :maxdepth: 2

   rbt/configuration
   rbt/commands/index
   rbt/aliases


.. _rbtools-api:

Python API
----------

Included with RBTools is a Python client for interacting with the Review Board
Web API.

.. note::
   This documentation assumes knowledge of the Review Board Web API. When
   possible links will be provided to relevant sections of the Web API
   documentation which can be found in the `Web API Guide`_.

.. _`Web API Guide`: http://www.reviewboard.org/docs/manual/dev/webapi/

.. toctree::
   :maxdepth: 2

   api/overview
   api/tutorial
   api/resource-specific


Installation
============

Before installing RBTools, you will need to have both Python and setuptools
installed.

We require Python 2.4 or higher. We recommend installing Python 2.7. The
3.x releases will not work.


Installing Python
-----------------

Linux
~~~~~

Python 2.x should come with your distribution. If not, or if 2.x isn't
installed, you will need to install the appropriate package. Please refer to
your package manager for the appropriate version.


Mac OS X
~~~~~~~~

Python 2.x comes pre-installed on Mac OS X.


Windows
~~~~~~~

You can install Python by running the latest `Python 2.7 Installer`_ for
Windows. We recommend the 32-bit MSI installer, as setuptools is not packaged
for 64-bit.

.. _`Python 2.7 Installer`: http://www.python.org/download/releases/2.7.3/


Installing setuptools
---------------------

Linux and Mac OS X
~~~~~~~~~~~~~~~~~~

To install setuptools on Debian_, Ubuntu_, or another Debian-based
distribution, type::

    $ apt-get install python-setuptools


To install on Fedora_ 8 and above, type::

    $ yum install -y python-setuptools-devel.noarch

To install on a `RedHat Enterprise`_, CentOS_, Fedora_ 7 and earlier, or
another RedHat-based distribution, type::

    $ yum install python-setuptools


Users of other distributions should check with their distribution for native
packages, or follow the `setuptools installation`_ instructions.

If the version of setuptools available for your distribution is older than
0.6c9, you'll need to install it first, and then upgrade it to the latest
version by running::

    $ easy_install -U setuptools


.. _`Python setuptools`: http://peak.telecommunity.com/DevCenter/setuptools
.. _`setuptools installation`: http://peak.telecommunity.com/DevCenter/EasyInstall#installation-instructions


Windows
~~~~~~~

You'll then need to run the latest `Python setuptools Installer`_ (look
toward the bottom of the page for the file listing).

Once Python and setuptools are installed, you may need to add a couple
directories to your system path.

1. Open :menuselection:`Start --> Control Panel` and navigate to the
   :guilabel:`System` icon.
2. Click on the :guilabel:`Advanced` tab.
3. Click :guilabel:`Environment Variables`.
4. Find :envvar:`PATH` in :guilabel:`System variables` and click
   :guilabel:`Edit`.
5. Add ``;C:\Python27;C:\Python27\Scripts`` (substitute your Python
   directory if it's not ``C:\Python27``) to the end of the list.

Depending on your version control system, you may also need to install the
command-line version of the client. Graphical clients like TortoiseCVS or
TortoiseSVN are not sufficient, and a ``cvs`` or ``svn`` binary is required.

.. _`Python setuptools Installer`: http://pypi.python.org/pypi/setuptools#windows


Installing RBTools
------------------

Once Python and Setuptools are installed, you can install RBTools just by
typing::

    $ easy_install -U RBTools


.. _Debian: http://www.debian.org/
.. _Ubuntu: http://www.ubuntu.com/
.. _`RedHat Enterprise`: http://www.redhat.com/
.. _Fedora: http://fedoraproject.org/
.. _CentOS: http://www.centos.org/


Installing GNU Diff
-------------------

Depending on your version control system, you may also need to install GNU
diff. Linux and Mac OS X should come with GNU diff pre-installed. On Windows,
you can use the `GNU Diffutils Installer`_

.. _`GNU Diffutils Installer`: http://gnuwin32.sourceforge.net/packages/diffutils.htm


Special Files
=============

The :command:`rbt` command stores its login session in a file called
``~/.rbtools-cookies``. It can also read this information from a file called
``~/.post-review-cookies.txt``, which was used by the deprecated
``post-review`` command.


Indices, Glossary and Tables
============================

* :ref:`glossary`
