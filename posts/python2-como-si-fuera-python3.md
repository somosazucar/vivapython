<!-- 
.. title: Python2 como si fuera Python3
.. slug: python2-como-si-fuera-python3
.. date: 2016-10-06 14:00:34 UTC-05:00
.. tags: python2, python3, trucos
.. category: 
.. link: 
.. description: 
.. type: text
.. author: icarito
-->

Para cualquier proyecto hoy en día es recomendable utilizar Python3 en vez de Python2, pero ocasionalmente uno encuentra una biblioteca incompatible o requiere utilizar un programa ya hecho que aún funciona únicamente en Python2.

```
from __future__ import (absolute_import, division,
                        print_function, unicode_literals)
import six
```

Con el encantamiento precedente, se consigue que el intérprete de Python2 se comporte en forma muy similar a como lo haría Python3. Mi característica favorita de Python3 es el manejo transparente de texto en *Unicode* para hacer caracteres acentúados - *áéíóú*.

Otra ventaja es que es una forma simple de ir moviendo código de Python2 a Python3, aún manteniendo soporte para Python2, ¡este código ahora seguramente será **de una vez compatible con Python3**!

Referencias:

* [Writing code for Python 2 and 3](http://matplotlib.org/devel/portable_code.html) - Sitio web de MatPlotLib 06/10/2016

