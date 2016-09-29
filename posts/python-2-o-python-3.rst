.. title: ¿Python2 o Python3?
.. slug: python-2-o-python-3
.. date: 2014-09-11 21:24:24 UTC-05:00
.. tags: faq, python2
.. link: 
.. description: 
.. type: text
.. author: icarito

Con frecuencia surge la interrogante al momento de empezar un proyecto, o mismo de aprender Python.

La pregunta es acertada puesto que en sus versiones mayores (el primer dígito del número de versión), los desarrolladores de Python aprovechan de hacer cambios importantes - e incompatibles.

.. TEASER_END

Por lo tanto, si tu programa corre en Python 2.1 lo más probable es que corra perfectamente en Python 2.7 pero no en Python 3.4 (que a la fecha es la última versión).

Lo que sucede es que desde el año 2000, cuando se publicó la versión 2.0 de Python, a la fecha, hay una serie de mejoras que se han querido introducir al lenguaje, las cuales no se podían hacer para "no romper la compatibilidad".

¿Qué cambios trae la versión 3?
===============================

Para nosotros, hispanohablantes, la mejora más relevante y drástica consiste en que Python 3.x trae soporte nativo y completo para texto en formato Unicode. En la versión 2, no podías poner caracteres con acentos en el código, ni siquiera en los comentarios, sin antes declarar una codificación en la primera línea de código.

Igualmente, obtenías los misteriosos errores tipo ``UnicodeDecodeError`` y ``UnicodeEncodeError``, si intentabas hacer operaciones sobre textos con acentos, sin tener el cuidado de primero convertir la cadena de texto al tipo ``unicode`` y luego decodificar con el codec ``utf-8``. En efecto, era doloroso.

Entre otros cambios positivos, las divisiones entre números enteros automáticamente devuelven un número con decimal (en Python-2, se truncaba el número hasta el siguiente entero menor).

La sintaxis en general de la biblioteca estándar ha mejorado en el sentido de ser más consistente. También, la sentencia ``input`` ahora hace lo esperable, solicitar una entrada al usuario. En Python-2 esto se hacía con ``raw_input``.

En general, por lo tanto, para aprender, Python 3 es lejos un mejor lenguaje.

¿En qué casos debería quedarme con la versión 2?
================================================

Si tienes que mantenerte compatible con plataformas donde solo se distribuya Python-2, (por ejemplo, las computadoras XO de OLPC). Si necesitas imperiosamente un módulo externo que sólo esté disponible para Python-2. Puedes comprobar si los módulos que te interesan están disponibles para Python 3 en la `Muralla de Superpoderes de Python 3
<https://python3wos.appspot.com/>`_.

¿Es muy malo quedarse en Python 2?
==================================

Si no tienes remedio, la verdad es que puedes irte preparando para una eventual futura migración. Los cambios incompatibles entre una versión y otra son significativos pero no demasiado extensos, de modo que portar tu código en el futuro no será demasiado fácil. Existen programas que intentan hacer los cambios en forma automática (buscar ``2to3``).
