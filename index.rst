Buildout para no iniciados (con screencast)
===========================================



Por Noe Nieto <nnieto@noenieto.com>

Revisiones
----------

 * 9 de Diciembre de 2011 (Primera Revisión)

Introducción
------------
.. class:: center

Buildout es una herramienta magnífica para construir software de
manera repetible.

Introducción (I)
----------------

.. class:: center

Buildout es una herramienta muy usada en las comunidades pythoneras
más experimentadas. Sirve para construir software de manera repetible.

Introducción (II)
-----------------

.. class:: center

Con Buildout es posible evitar aquellas situaciones
donde una pieza de software funciona bien en la máquina de un
desarrollador, pero no en la máquina de otro desarrollador por que
faltan ciertas librerías o las librerías que tiene instaladas tienen
otra versión.

Módulos y el  *Python path*
---------------------------

.. class:: incremental

 * Módulos - Concepto importantísimo para entender el funcionamiento
   de Python.

 * Un archivo con extensión ``.py``

 * Una carpeta con un archivo ``__init__.py``

Módulos y el *Python path* (I)
------------------------------

Al ejecutar::

   import mi_modulo

.. class:: incremental

 * Primero busca ``mi_modulo.py`` en el directorio que contiene el
   script que se está ejecutando o en el directorio donde se invocó
   ``python``.

 * Después busca en la lista de directorios definida por la variable
   de entorno ``PYTHONPATH``.

 * Si no existe ``PYTHONPATH`` la búsqueda continua en
   ``/usr/lib/python`` o ``/usr/local/lib/python``.


Módulos y el *Python path* (II)
-------------------------------

Las tres anteriores rutas de búsquedas están contenidas en la variable
``sys.path``.

Módulos y el *Python path* (III)
--------------------------------

Ejemplo::

  >>> import sys
  >>> for p in sys.path:
  ...     print p
  ... 

Módulos y el *Python path* (IV)
-------------------------------

::

  /usr/lib/python27.zip
  /usr/lib/python2.7
  /usr/lib/python2.7/plat-linux2
  /usr/lib/python2.7/lib-tk
  /usr/lib/python2.7/lib-old
  /usr/lib/python2.7/lib-dynload
  /usr/lib/python2.7/site-packages

Paquetes de sotfware Python (eggs)
-----------------------------------

*"Eggs are to Pythons as Jars are to Java..."*

* Sirven para distribuir proyectos de software escritos en Python y
  agregar información adicional.

  * Dependencia de otros *eggs*.

  * Plugins.

  * Versión.

Distutils
---------

.. class:: incremental

 * Viene incluido en Python por default.

 * Herramientas para distribuir software.

   * Metadatos (Autor, licencia, etc).

   * Ayudantes para construir paquetes distribuibles a partir del
     código fuente.

Distutils (I)
-------------

.. class:: incremental

 * Pero ``distutils`` solo sirve para un solo paquete.

 * No hay manera de definir dependencias hacia otros paquetes de
   software.


SetupTools
----------

Buildout
--------


Final
-----

 * Noe Nieto <nnieto@noenieto.com>

 * http://noenieto.com/blog/buildout-para-no-iniciados-con-screencast

 * Esta presentación la hice con ``python-docutils``, ReSTructuredText
   y emacs.




