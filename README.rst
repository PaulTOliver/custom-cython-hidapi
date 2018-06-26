cython-hidapi
=============

Description
-----------

A Cython interface to `CUSTOM HIDAPI <https://github.com/paultoliver/hidapi>`_ library.

Software Dependencies
---------------------

* `Python <http://python.org>`_
* `Cython <http://cython.org>`_
* hidraw

License
-------

cython-hidapi may be used by one of three licenses as outlined in LICENSE.txt

Build from source
-----------------

1. Download cython-hidapi archive::

    $ git clone https://github.com/paultoliver/cython-hidapi.git
    $ cd cython-hidapi

2. Download custom hidapi::

    $ git clone https://github.com/paultoliver/hidapi.git

3. Build cython-hidapi extension module. To use hidraw API instead of libusb add --without-libusb option::

    $ python setup.py build --without-libusb

4. Install cython-hidapi module into your Python distribution::

    $ sudo python setup.py install

5. Test install::

    $ python
    >>> import hid
    >>> hid.enumerate()

Udev rules
----------

For correct functionality under Linux, you need to create a rule file similar
to `this one <https://raw.githubusercontent.com/trezor/trezor-common/master/udev/51-trezor.rules>`_
in your udev rules directory.

Also you might need to call ``udevadm control --reload-rules`` to reload the rules.
