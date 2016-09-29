.. title: Generando sitios con Nikola
.. slug: generando-sitios-con-nikola
.. date: 2014-09-08 11:32:35 UTC-05:00
.. tags: programas, private
.. link: 
.. description: 
.. type: text

Ocasionalmente uno encuentra programas realmente útiles hechos en Python.

Uno de ellos es el generador de sitios web estáticos Nikola_.

Nos parece oportuno rendir homenaje a este software porque es el motor que hace funcionar a *Viva Python*.
https://www.google.com/adsense/app#homehttps://www.google.com/adsense/app#home
Para quienes conocen software de publicación como Wordpress (que es muy bueno), les contamos que Nikola es mucho más simple.

Primero lo primero
==================

La principal idea detrás de Nikola es que el autor se enfoque en lo que desea escribir.

Para inicia un nuevo sitio, se utiliza el comando ``nikola init``:

  $ nikola init
  Creating Nikola Site
  ====================

  This is Nikola v7.1.0.  We will now ask you a few easy questions about your new site.
  If you do not want to answer and want to go with the defaults instead, simply restart with the `-q` parameter.
  --- Questions about the site ---
  Destination: mi_sitio
  Site title [My Nikola Site]: Mi Sitio Chocolate
  Site author [Nikola Tesla]: Chocolatero
  Site author's e-mail [n.tesla@example.com]: chocolate@example.com
  Site description [This is a demo site for Nikola.]: Todo sobre el chocolate
  Site URL [http://getnikola.com/]: http://chocolatero.example.com/
  --- Questions about languages and locales ---
  We will now ask you to provide the list of languages you want to use.
  Please list all the desired languages, comma-separated, using ISO 639-1 codes.  The first language will be used as the default.
  Type '?' (a question mark, sans quotes) to list available languages.
  Language(s) to use [en]: es

  Please choose the correct time zone for your blog.  Nikola uses the tz database.
  You can find your time zone here:
  http://en.wikipedia.org/wiki/List_of_tz_database_time_zones

  Time zone [UTC]: America/Bogota
  Current time in America/Bogota: 23:38:14
  Use this time zone? [Y/n] Y
  --- Questions about comments ---
  You can configure comments now.  Type '?' (a question mark, sans quotes) to list available comment systems.  If you do not want any comments, just leave the field blank.
  Comment system: 

  That's it, Nikola is now configured.  Make sure to edit conf.py to your liking.
  If you are looking for themes and addons, check out http://themes.getnikola.com/ and http://plugins.getnikola.com/.
  Have fun!
  [2014-09-09T04:38:24Z] INFO: init: Created empty site at mi_sitio.


Nikola no proporciona ninguna interfase de usuario más allá de este programa de terminal. P

Luego ejecuta ``nikola build`` y *voilá*, Nikola se encarga de combinar las plantillas HTML con los archivos de texto, crear las páginas de índice, el archivo histórico, las etiquetas, etc, y finalmente de copiar todo el resultado a la carpeta ``output/``.

Para crear un nuevo artículo se usa el comando ``nikola new_post``.

Si queremos ver el resultado basta con ingresar ``nikola auto`` y abrir un navegador apuntando a `http://localhost:8000/`.

.. _Nikola: http://getnikola.org/
