<!-- 
.. title: Automatízate con Virtualenv y Direnv
.. slug: automatizate-con-virtualenv-y-direnv
.. date: 2016-09-29 01:22:23 UTC-05:00
.. tags: python3,virtualenv,bibliotecas,trucos
.. category: 
.. link: 
.. description: 
.. type: text
-->

Una forma conveniente de elegir entre Python2 y Python3 es crear un ambiente virtual `virtualenv`.

**Virtualenv** es una herramienta que permite crear una copia del entorno Python, aislada de la del sistema operativo de base.

Esto es útil para utilizar un entorno Python de una versión diferente a la del sistema. También lo es para evitar instalar en el sistema paquetes de bibliotecas que solo se necesitan para un proyecto particular. Finalmente se evita el problema de cuando una actualización deja inservible un programa por éste depender de una versión anterior de las bibliotecas del sistema.

**Direnv** permite automatizar el proceso (algo tedioso) de crear y recordar activar el ambiente virtual para cada proyecto (aquí concebido como directorio).

```
$ sudo apt install direnv virtualenv # en Debian y derivados
```

## Direnv para automatizar todo

Una vez instalados los paquetes respectivos, es necesario hacer algunos ajustes al intérprete de comandos de la terminal (generalmente *bash*):

```
$ direnv hook bash
$ echo 'export EDITOR="gedit"' > ~/.bashrc
```

Es necesario definir la variable de entorno EDITOR con el nombre de nuestro editor de preferencia, y por ello la hemos colocado en el *script* de arranque de *bash*, `~/.bashrc` la referencia a *gedit*. Abra una nueva terminal para que estos cambios queden aplicados al entorno.

### Y la magia es...

Primero creamos y/o entramos a un directorio de proyecto, `mkdir -p ruta/a_mi_proyecto/ && cd ruta/a_mi_proyecto/`.

Luego crearemos la definición de entorno con el comando `direnv edit .`.

Entramos lo siguiente en el editor vacío que se abrirá editando el archivo `.envrc`:

```
layout python
```

o para Python 3:

```
layout python3
```

Cabe resaltar que además de esta directiva interna de `direnv`, es posible colocar en este archivo todo tipo de comandos bash, los cuales se ejecutarán toda vez que se acceda al directorio.

El resultado:

```
direnv: loading .envrc
Running virtualenv with interpreter /usr/bin/python
New python executable in /home/icarito/Proyectos/zyngo_sol/.direnv/python-2.7.12+/bin/python
Installing setuptools, pkg_resources, pip, wheel...direnv: ([direnv export bash]) is taking a while to execute. Use CTRL-C to give up.
done.
direnv: export +VIRTUAL_ENV ~PATH
```

Podrás comprobar que el intérprete de Python corre desde el entorno virtual con `which python`. Podrás instalar bibliotecas de Python en tu ambiente virtual sin interferir con tu sistema operativo. Cuando dejes el directorio, el ambiente se restaurará.

Como referencia aquí dejo:
- La documentación de `direnv`: https://github.com/direnv/direnv
- Algunas notas específicas sobre Python y direnv: https://github.com/direnv/direnv/wiki/Python
