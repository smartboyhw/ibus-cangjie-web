**********
Installing
**********

Installing IBus Cangjie should be trivial. We want you to start using it as
easily and quickly as possible, not to spend time battling with tarballs and
packages.

The instructions provided here will vary depending on your Operating System,
so make sure you're reading the right one.

.. note:: If your favourite Operating System is not listed here, but it
          nevertheless provides an easy way to install IBus Cangjie, please
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

    # yaourt -S ibus-cangjie

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

*TODO: write this up*

----

.. Sphinx doesn't want us to end on a transition, so here is a comment.
