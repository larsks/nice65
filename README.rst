This is a fork of https://github.com/mnaberez/py65 since the author blocked me
when I tried to submit a pull request. Please direct any bug reports or pull
requests to this repository and I will do my best to handle them in a polite
and respectful fashion.

Nice65
====

Nice65 provides tools for simulating hardware based on 6502-like
microprocessors.  It has the following goals:

- Focus on ease of use and modularity rather than performance.  Nice65 is
  written in the Python programming language for productivity, while
  similar programs are written in C for performance.

- Enable simulations to be created for systems where it might have
  otherwise not been practical, such as homebuilt computers.

- Rigorously unit test all of the components.  While the tools provided
  by Nice65 may not always be perfect, their behavior is verified through
  tests so unexpected results are minimized.

Installation
------------

Nice65 packages are `available <http://pypi.python.org/pypi/nice65>`_ on the
Python Package Index (PyPI).  You download them from there or you can
use ``pip`` to automatically install or upgrade Nice65::

    $ pip install -U nice65

Devices
-------

The following devices are simulated at this time:

- ``mpu6502`` simulates the original NMOS 6502 microprocessor from MOS
  Technology, later known as Commodore Semiconductor Group (CSG). At this
  time, all of the documented opcodes are supported.  Support for the
  illegal opcodes is planned for the future.

- ``mpu65c02`` simulates a generic CMOS 65C02 microprocessor. There were
  several 65C02 versions from various manufacturers, some with more
  opcodes than others. This simulation is based on the W65C02S from the
  Western Design Center (WDC).

- ``mpu65org16`` simulates the 65Org16, a 6502-like microprocessor with a
  16-bit data bus and 32-bit address bus.  This microprocessor is a project
  of the `6502.org community <http://forum.6502.org/viewtopic.php?t=1824>`_
  and a `Verilog core <https://github.com/BigEd/verilog-6502/wiki>`_ for it
  has been implemented.

Monitor
-------

Nice65 includes a console-based machine language monitor (sometimes also called
a debugger).  This program, ``nice65mon``, allows you to interact with the
simulations that you build.  Its features include:

- Commands that are largely compatible with those used in the monitor of
  the popular VICE emulator for Commodore computers.

- Ability to load, dump, and fill memory.

- Simple assemble and disassemble capability, including support for labels
  and labels with offsets.

Documentation
-------------

Nice65 documentation is written using `Sphinx <http://sphinx.pocoo.org/>`_ and
is published to `http://nice65.readthedocs.org/
<http://nice65.readthedocs.org/>`_.
