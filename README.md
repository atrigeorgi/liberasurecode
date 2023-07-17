liberasurecode
==============

I tried to run the liberasurecode on Apple M2 but I had two errors:
* a function declaration without a prototype is deprecated in all versions of C [-Werror,-Wstrict-prototypes]
* function pointer incompatible pointer types void (*)(void *) from void (my_type *)

Solutions:
* put void as parameters with functions that do not have parameters.
* remove /test folder
----


Active Users
====================

 * PyECLib - Python EC library: https://github.com/openstack/pyeclib
 * Openstack Swift Object Store - https://wiki.openstack.org/wiki/Swift


----

Build and Install
=================

Install dependencies -

 Mac hosts:
```sh
 $ brew install autoconf automake libtool
```

Install repository:
```sh
 $ git clone https://github.com/openstack/liberasurecode
 $ cd liberasurecode
```

To build the liberasurecode repository, perform the following from the 
top-level directory:

``` sh
 $ ./autogen.sh
 $ ./configure --prefix=/usr/local
 $ make
 $ make test
 $ sudo make install
```
