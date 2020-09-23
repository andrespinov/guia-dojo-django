# Guía de Instalación - Dojo Django

## Windows

### Instalar Pyhton
Para instalar Python en Windows debemos descargar el instalador [desde la página oficial](https://www.python.org/downloads/).

![](images/image1.png?raw=true)

Esto deberá descargar un archivo con extensión .exe, lo ejecutamos. Antes de continuar con la instalación asegurate de seleccionar la opción **Add Python 3.8 to PATH**, así no tendremos que configurar Python en nustro PATH manualmente.

![](images/image2.png?raw=true)

Presionamos la opción de **Install Now** y esperamos.

![](images/image3.png?raw=true)

Luego finalizamos la instalación presionando **Close**.add

Después de finalizar la instalación, abrimos una lina de comandos como cmd o powershell para verificar la instalación y la version de Python.

```powershell
> py --version
```

Ésto debe arrojar como respuesta **Python 3.8.4** (o la versión de Python que se haya descargado en el instalador). Si el comando no existe se recomienda reiniciar las lineas de comando o todo el sistema operativo para que el PATH sea recargado.

Finalmente en el dojo se hara uso de los ambientes virtuales de python para ello utilizaremos venv, para probar el uso de ambientes virtuales cree una carpeta de pruebas

```bash
PS> mkdir prueba
PS> cd prueba
PS> py -m venv ambiente-prueba
```

Para activar el ambiente ejecute

```bash
PS> .\ambiente-prueba\Scripts\activate
```

Para confirmar que está haciendo uso del ambiente virtual debe verificar que el interprete de python tiene la ruta del ambiente virtual.

```bash
PS> where python
../ambiente-prueba/bin/python.exe
```

Para desactivar el ambiente virtual ejecute

```bash
PS> deactivate
```

## Linux

Por defecto la mayoria de distribuciones de Linux tienen instalado python3, para verificarlo utilice

```bash
$ python3 --version
```

En caso de tener obtener un error instale python3 siguiendo las instrucciones

```bash
$ sudo apt update
$ sudo apt install python3.6
```

Para obtener una versión más reciente de python ejecute

```bash
$ sudo apt install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt update
$ sudo apt install python3.8
```

En caso de tener un sistema Mac, debe instalar primero homebrew para ello utilice

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

y ejecute

```bash
$ brew install python3
```

Además de python necesitaremos pip3, al instalar python3 ya lo tendremos disponible, para verificar utilice

```bash
$ pip3 --version
```
En caso de no tener pip3 ejecute

```bash
$ sudo apt install python3-pip
```

Finalmente en el dojo se hara uso de los ambientes virtuales de python para ello utilizaremos venv, para probar el uso de ambientes virtuales cree una carpeta de pruebas

```bash
$ mkdir prueba
$ cd prueba

$ python3 -m venv ambiente-prueba
```

Para activar el ambiente ejecute

```bash
$ source ambiente-prueba/bin/activate
```

Para confirmar que está haciendo uso del ambiente virtual debe verificar que el interprete de python tiene la ruta del ambiente virtual.

```bash
$ which python
../ambiente-prueba/bin/python
```

Para desactivar el ambiente virtual ejecute

```bash
$ deactivate
```

