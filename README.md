fourpiskytools
==============

A handful of simple convenience functions tying together use of the
[voevent-parse](http://voevent-parse.readthedocs.org/) and 
[Comet](http://comet.transientskp.org/) 
packages, providing a 
quick and easy way to get started sending or receiving VOEvents with the
[4 Pi Sky](http://4pisky.org) 
VOEvent broker (or indeed any VOEvent node of your choice).

This package should be considered 'highly opinionated': it makes
many assumptions about what you want to do, in order to present a
simple interface.
Those with more specific requirements should refer to this package as
a quick example, and then use *voevent-parse* and *Comet* directly
(see also: [pysovo](https://github.com/timstaley/pysovo)).

Features
--------
* A function provding a *subprocess* wrapper about *comet-sendvo*, to allow
  publishing of [VOEvents](http://en.wikipedia.org/wiki/VOEvent) from a scripted
  process.
* A simple (~3 lines) routine for generating unique identifiers to tag your
  VOEvents with.
* A couple of ready-made functions that take a dictionary defining the sender's 
  'identity' and provide one-liner methods for composing VOEvent packets.
* A basic utility class for generating GTK notifications (desktop alerts
  akin to e.g. the 'new email' pop-up that Thunderbird will generate).

That's it - the package is intentionally minimal.
 

Installation
------------
A [virtualenv](http://virtualenv.readthedocs.org/en/latest/virtualenv.html)
is recommended, but not essential.
I also recommend use of
[pip](http://pip.readthedocs.org/en/latest/quickstart.html)
since it allows easy version checking and package uninstallation.

Note that *lxml*
(which is a dependency which *pip* will attempt to install for you)
has some prerequisites for compilation that can cause a
standard ``pip install``
to fail with somewhat cryptic errors.
On Ubuntu you can satisfy those requirements by running:

    apt-get install libxml2-dev libxslt-dev

before you attempt to install anything else.

Once you've checked out the code, from the package root directory run:

    pip install .
    

Or if you prefer the traditional method:

    python install setup.py

If you run into problems, try consulting the installation guides for
[voevent-parse](http://voevent-parse.readthedocs.org/en/master/intro.html#installation)
and
[Comet](http://comet.transientskp.org/en/1.2.1/installation.html)
and verify that you can install those packages individually.


Usage
-----
See the [examples](examples).
