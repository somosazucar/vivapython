.. title: Instala Python
.. slug: instala-python
.. date: 2014-09-15 09:35:01 UTC-05:00
.. tags: guia
.. link: 
.. description: 
.. type: text

El sitio donde siempre podrás encontrar la última versión de Python es la `página oficial de descargas de Python 
<https://www.python.org/download>`_.

Hemos autodetectado que tu plataforma parece ser:

.. TEASER_END

.. raw:: html

    <script>
        var platform = navigator.platform
        var ua = navigator.userAgent
        var isAndroid = ua.indexOf("android") > -1;
        if (isAndroid) {
            platform = "Android"
            }
        var isGNU = platform.indexOf("Linux") > -1;
        if (isGNU) {
            platform = "GNU+Linux"
            }

        document.write (platform)
    </script>

Pero no nos tomes la palabra, tu sabrás esto mejor que nosotros, o derrepente necesitas descargar una versión para otro sistema operativo.

Si tu plataforma es Windows
===========================

Ninguna versión de Windows trae el intérprete de Python instalado. Por lo tanto tendrás que descargarlo e instalarlo por tu cuenta.

La versión recomendada a la fecha es `Python 3.4.1 - 32bits
<https://www.python.org/ftp/python/3.4.1/python-3.4.1.msi>`_.

Solo se recomienda la versión de 64 bits si esperas consumir más de 4GB de memoria RAM en tu programa.

Si tu plataforma es Mac OSX
===========================

El sistema de los Mac trae Python2 instalado. Si deseas, puedes instalar `Python 3.4.1 - 32/64 bits
<https://www.python.org/ftp/python/3.4.1/python-3.4.1-macosx10.6.dmg>`_.

Si tu plataforma es GNU+Linux
=============================

¡Estás de suerte! Si tu sistema es medianamente reciente, seguramente tienes tanto Python2 como Python3 instalado. Intenta ejecutar desde la terminal ``python2`` y ``python3`` para verificar qué versión tienes instalada.

Si encuentras que estás desactualizado, consulta los repositorios de tu distribución.

Si tu plataforma es Android
===========================

Te recomendamos desarrollar tus programas desde una computadora convencional, y luego empaquetarlos para Android. Para ello hay una herramienta genial llamada Kivy.

Sin embargo, existe un entorno de desarrollo llamado QPython, hecho en Kivy, el cual incluye un intérprete y un editor: `QPython 0.9.8 para Android
<http://qpython-bin.googlecode.com/git/QPython80.apk>`_.

Otras opciones
==============

Existen intérpretes alternativos, diferentes versiones, otras plataformas, etc. 

Encuentra más información en la `página oficial de descargas de Python 
<https://www.python.org/download>`_.

