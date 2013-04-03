**********
Installing
**********

Installing IBus Cangjie should be trivial. We want you to start using it as
easily and quickly as possible, not to spend time battling with tarballs and
packages.

.. note:: Once you installed IBus Cangjie, you will need to restart IBus so it
          finds the new engine. The easiest way to do this is to just reboot
          your computer, or log out and then log back in.

The instructions provided here will vary depending on your Operating System,
so make sure you're reading the right one.

If your favourite Operating System is not listed below, but it nevertheless
provides an easy way to install IBus Cangjie, please
:ref:`let us know <talk-to-us>`.

If we don't provide instructions for your Operating System, you can always
refer to the last part and install :ref:`from the sources <sources>`.

----

Arch Linux
==========

.. note:: IBus Cangjie is not in one of the main Arch Linux repositories, but
          only in AUR. As such, you will first need to install `yaourt`_.

.. warning:: This AUR package will effectively build the IBus Cangjie sources
             straight from the development branch of the Git repository.
             Proceed with caution.

To install IBus Cangjie on Arch Linux, simply run the following command as root::

    # yaourt -S ibus-cangjie-git

.. _yaourt: https://wiki.archlinux.org/index.php/Yaourt

Fedora
======

.. warning:: IBus Cangjie is not in Fedora yet, but only in a third-party
             repository. This repository is maintained by one of the core
             developers, so it should be relatively safe. Nevertheless,
             proceed with caution.

To install IBus Cangjie on Fedora, simply run the following commands as root::

    # wget http://repos.fedorapeople.org/repos/bochecha/ibus-cangjie/fedora-ibus-cangjie.repo -O /etc/yum.repos.d/fedora-ibus-cangjie.repo
    # yum install ibus-cangjie

.. _sources:

From the sources
================

The first thing to do is to get the source code, either by downloading the
latest release tarball, or by cloning the Git repository.

In order to install and use IBus Cangjie, you will need the following to be
installed on your system first:

* `Python <http://python.org>`_ >= 3.2
* `IBus <https://code.google.com/p/ibus/>`_ >= 1.4.1
* `pygobject <https://live.gnome.org/PyGObject>`_ built for Python 3
* `libcangjie <https://github.com/wanleung/libcangjie>`_
* `pycangjie <https://github.com/bochecha/pycangjie>`_
* `pycanberra <https://github.com/psykoyiko/pycanberra>`_ (optional)

  * This is only needed to give some feedback to the user by playing an error
    sound on incorrect inputs. If you don't have this installed, then IBus
    Cangjie just won't play any sound.
  * Please note that we need a Python 3 version of pycanberra, see this
    (yet-unmerged) `pull request <https://github.com/psykoyiko/pycanberra/pull/2>`_.

Build from a release tarball
----------------------------

.. note:: There are currently no stable release of IBus Cangjie, the sources
          can only be obtained from Git.

All release tarballs are available `in the same folder`_.

We highly recommend you always use the latest release.

IBus Cangjie is a regular Autotools project, so it should be possible to build
it with the usual commands::

    $ ./configure
    $ make
    # make install

Make sure you read about the :ref:`build caveats <build-caveats>`.

.. _in the same folder: http://ibus-cangjie.opensource.hk/releases/

Build from a Git clone
----------------------

The first thing to do is to clone the Git repository::

    $ git clone git://github.com/bochecha/ibus-cangjie

Alternatively, if you forked IBus Cangjie on Github, then do::

    $ git clone git@github.com:<your github nickname>/ibus-cangjie

If you cloned your fork, we highly recomment you keep a reference on the
central repository. You can do that with the following commands, from inside
your clone::

    $ git remote add upstream git://github.com/bochecha/ibus-cangjie
    $ git fetch upstream

This will help you fetch the latest changes we made, and rebase your work on
top of it.

Then, building is the usual sequence of commands for Autotools-based
projects::

    $ ./autogen.sh
    $ make
    # make install

Make sure you read about the :ref:`build caveats <build-caveats>`.

.. _build-caveats:

Mind the caveats
----------------

Install prefix
..............

By default, the Autotools will usually set the install prefix to
``/usr/local``. However, IBus seems to only find engines if installed in the
``/usr`` prefix.

As such, we recommand you pass the appropriate option to either the
``configure`` or ``autogen.sh`` script, as follows, either::

    $ ./configure --prefix=/usr

or::

    $ ./autogen.sh --prefix=/usr

This means IBus Cangjie will be installed in the system prefix, which is
normally the territory of your package manager (e.g ``yum`` or ``apt-get``).

That's not ideal, but it is necessary until we figure out what the problem is,
and how to get IBus to load engines from ``/usr/local``.

----

.. Sphinx doesn't want us to end on a transition, so here is a comment.
