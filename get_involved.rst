****************
Getting involved
****************

As any other Free Software project, we welcome anybody to come and join us.

Feel free to provide us your ideas and feedback.

And if you feel like hacking, keep the patches coming!

----

.. _talk-to-us:

Come talk to us
===============

We currently do not have any dedicated communication forum for IBus Cangjie.

Nevertheless, it shouldn't be too hard to reach us.

We are available:

* by email, in `the Google Group for the Hong Kong LUG`_
* by IRC, in the ``#linux-hk`` and ``#ibus`` channels on Freenode

.. _the Google Group for the Hong Kong LUG: https://groups.google.com/forum/?fromgroups#!forum/hklug

----

Report bugs
===========

We use the Github facilities to track `our bugs`_.

If your issue is not reported yet, please `open a new ticket`_.

Try to explain in details how to reproduce the problem. If we can't reproduce
it, it is very unlikely that we'll be able to fix it.

Also, please be polite. We are much more likely to listen to calm,
constructive criticism than to random rants and insults. If you want to vent,
do it on your own blog.

That being said, don't hesitate to suggest us how we could do things better.
User feedback, both positive and negative, is one of the most valuable things
we can receive. Remember, we're working on IBus Cangjie for you, the users. We
need to know what we're doing right and where we can improve!

.. _our bugs: https://github.com/bochecha/ibus-cangjie/issues?state=open
.. _open a new ticket: https://github.com/bochecha/ibus-cangjie/issues/new

----

Hack the code
=============

We host `our development at Github`_. Fork away and open pull requests, or
just clone the Git repositories and attach patches in bug reports.

Be sure to test your changes before sending them. The best way to do that is
to :ref:`build and install the sources <sources>` after you made your
modifications. Build from Git though, not from the release tarballs.

In any case, try to open a bug report for each issue you want to work on, or
assign any existing bug report to yourself. This helps us know that you're
interested in working on this, so that we don't do it at the same time.

We try to pay attention to having good commit messages. Be sure to read
Peter Hutterer's great post about `writing good commit messages`_.

Basic Python 3 skills should be all you need to start hacking on IBus Cangjie.
However, some things might need to be done in `libcangjie`_, the underlying
library providing the Cangjie mapping, or `pycangjie`_, its Python bindings.
These will require some C++ and Cython knowledge respectively, but nothing
terrible.

.. _our development at Github: https://github.com/bochecha/ibus-cangjie/
.. _writing good commit messages: http://who-t.blogspot.hk/2009/12/on-commit-messages.html
.. _libcangjie: https://github.com/wanleung/libcangjie/
.. _pycangjie: https://github.com/bochecha/pycangjie/

----

Translate
=========

We use `Transifex`_ for our translations.

If you want to `translate IBus Cangjie in your language`_, it all happens there.

.. _Transifex: https://www.transifex.com
.. _translate IBus Cangjie in your language: https://www.transifex.com/projects/p/ibus-cangjie/

----

Hack the website
================

Just like the code, this website is Free Software, `hosted at Github`_.

If you notice any issue with it, or want to help make it better, send patches
or pull requests.

.. _hosted at Github: https://github.com/bochecha/ibus-cangjie-web/
