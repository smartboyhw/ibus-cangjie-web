**************************
Frequently Asked Questions
**************************

We hope you can find the answers you need on this page.

If not, just come and :ref:`ask us <talk-to-us>`.

.. note:: You can use the "**Page**" button in the top banner to quickly
          review each question.

----

General questions about IBus Cangjie
====================================

Who is IBus Cangjie designed for?
---------------------------------

Because **Hong Kong people writing Traditional Chinese** represent the vast
majority of the Cangjie and Quick users, they are the primary target of
IBus Cangjie.

Others can still use it though, and we certainly will make everything we can
to give them a great user experience too when possible.

Everything is a matter of compromise. Having a primary design target means
that if some use cases conflict, we will lean towards the needs of the Hong
Kong users.

On what systems does IBus Cangjie run?
--------------------------------------

IBus Cangjie should provide an excellent user experience on **all modern
platforms where IBus runs**.

If it doesn't, **please consider this as a bug and report it**. We really want
to run on as many platforms as possible and to provide a consistent user
experience to all IBus users.

The main developers currently use GNOME, so this is where most of our efforts
go, and we might not be able to do the necessary integration work for other
environments. But patches to make IBus Cangjie work beautifully everywhere
will be warmly welcome.

What was the motivation for starting IBus Cangjie?
--------------------------------------------------

Before answering this question, one must first understand the current status
at the time where we started writing IBus Cangjie.

The Cangjie and Quick input methods have traditionally been provided in IBus
by an engine called `ibus-table`_.

The biggest advantage of ibus-table is that it is a **generic** engine: you
pass it tables, it somehow gives you an input method user experience.

And because it is generic, it can work with **any kind of tables**. There are
currently tables for `Chinese languages`_, tables for
`emoticons or the International Phonetic Alphabet`_,...

All of these cover very different languages and needs, but `ibus-table`
somehow manages to implement a "decent enough" user experience for all of
them.

However, its genericity is also its biggest problem: `ibus-table` can either
implement some kind of "*lowest common denominator*" behaviour, or it risks
becoming extremely complex if it tries to special-case the very different
needs of every input method. And in fact, it goes to great lengths trying to
implement some specific behaviours, which turns its code into a big, messy
spaghetti.

We believe that `ibus-table` is a great "first step" to have something working
very quickly. That's what we had for years for Cangjie and Quick, and it was
"decent enough".

But **we didn't want "decent enough" any more**.

We believe that all users deserve an excellent user experience, especially
when it comes to something as critical as inputting text in their native
language.

As such, the time came to start working on a **dedicated, specialized** engine
for Cangjie and Quick which, because it is tailor-made to these input methods,
can provide users the best possible inputting experience, allowing to type
quickly, and comfortably.

.. _ibus-table: https://github.com/kaio/ibus-table/
.. _Chinese languages: https://github.com/definite/ibus-table-chinese
.. _`emoticons or the International Phonetic Alphabet`: https://github.com/moebiuscurve/ibus-table-others

----

Help
====

Why are all the keys I input doubled?
-------------------------------------

This is most likely caused by a `known bug on 32 bits system`_.

It is fixed in ``pygobject`` >= 3.7.91, but as many distributions still ship
an older version, we work around the bug in IBus Cangjie.

Make sure you are running a recent enough version of IBus Cangjie, as the
workaround was introduced only recently in Git.

The first stable release of IBus Cangjie will include the workaround.

.. _known bug on 32 bits system: https://bugzilla.gnome.org/show_bug.cgi?id=693121

Why can't I find IBus Cangjie in the GNOME Settings?
----------------------------------------------------

One possibility is that you didn't install IBus Cangjie. If that's the case,
:doc:`learn how to do that <install>`.

If you are sure you installed it, and it still doesn't appear, then this is
most likely because you are using GNOME 3.6.

GNOME 3.6 has its own whitelist of input sources which are recognized to be
well maintained and provide a great user experience, and unfortunately,
IBus Cangjie was started after GNOME 3.6 was released.

As such, there is one additional hoop you will need to jump through after
installing IBus Cangjie in a GNOME 3.6 environment.

Do not fear though, as it is not too hard (and again, it should not be
necessary any more after GNOME 3.8). All you have to do is as follows:

#. In the Activities overview, search for the word "terminal", and run the
   *Terminal* application.

#. In there, run the following command::

    $ gsettings set org.gnome.desktop.input-sources show-all-sources true

#. Close the Terminal application

You will now find many more input methods in the GNOME Settings, among which
will be the Cangjie and Quick input methods provided by IBus Cangjie.

Where is the option to use half-width characters on GNOME?
----------------------------------------------------------

Are you using GNOME 3.6?

The 3.6 release was the very first time GNOME developers tried to integrate
input methods into the desktop, and as such it is suffering from a lot of
issues.

One of these is that there is no support for engine properties. These are the
options you change quickly, while typing, without having to go change the
Settings all the time.

The half-width characters option is such a property, and that means it can't
be used on GNOME 3.6.

Fortunately, this is fixed in GNOME 3.8, so we recommend you upgrade.
