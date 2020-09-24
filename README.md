# Guía de Instalación - Dojo Django

## Windows

### Instalación de Python

Para instalar Python en Windows debemos descargar el instalador [desde la página oficial](https://www.python.org/downloads/).

![](images/image1.png?raw=true)

Esto deberá descargar un archivo con extensión .exe, lo ejecutamos. Antes de continuar con la instalación asegurate de seleccionar la opción **Add Python 3.8 to PATH**, así no tendremos que configurar Python en nustro PATH manualmente.

![](images/image2.png?raw=true)

Presionamos la opción de **Install Now** y esperamos.

![](images/image3.png?raw=true)

Luego finalizamos la instalación presionando **Close**.

Después de finalizar la instalación, abrimos una línea de comandos como cmd o PowerShell para verificar la instalación y la version de Python.

```powershell
> py --version
Python 3.8.4
```

Ésto debe arrojar como respuesta **Python 3.8.4** (o la versión de Python que se haya descargado en el instalador). Si el comando no existe, se recomienda reiniciar las lineas de comando o todo el sistema operativo para que el PATH sea recargado.

### Configuración del ambiente virtual

En el dojo se hará uso de los ambientes virtuales de Python, para ello utilizaremos venv. Esta herramienta ya viene con la librería estándar de Python desde la versión 3.3.

Para crear el ambiente virtual, primero creamos un nuevo directorio y luego procedemos a generar el ambiente virtual

```bash
PS> mkdir dojo-django
PS> cd dojo-django
PS> py -m venv ambiente-dojo
```

Este comando creará un directorio con el nombre **ambiente-dojo**, el cual contiene archivos de configuración pertenecientes al ambiente virtual.

### Activar el ambiente virtual

Luego debemos activar el ambiente para poder trabajar sobre él. Ésto se hace ejecutando el archivo **activate** en el directorio de Scripts que se generó al crear el ambiente virtual.

```bash
PS> .\ambiente-dojo\Scripts\activate
```
> Note que la navegación entre directorios en Windows es usando el caracter **\\** y no del caracter **/** como normalmente lo hacemos en la  web y en sistemas Unix.

Para confirmar que se está haciendo uso del ambiente virtual, puede observar que al prompt de la linea de comandos se le agrega un prefijo con el nombre del ambiente.

```bash
(ambiente-prueba) PS>
```

También lo puede confirmar verificando que el interprete de Python tenga la ruta del ambiente virtual creado.

```bash
(ambiente-prueba) PS> where python
./ambiente-dojo/Scripts/python.exe
```

### Instalación de Django

Luego procedemos a la instalación de django dentro del ambiente virtual

```bash
(ambiente-prueba) PS> pip install django
```

### Desativar el ambiente virtual

Cuando ya no necesitemos trabajar sobre el ambiente virtual, lo debemos desactivar para evitar confusión en la instalación de librerías.

Para desactivar el ambiente virtual ejecute.

```bash
(ambiente-prueba) PS> deactivate
```

## Linux

### Instalación de Python

Por defecto la mayoria de distribuciones de Linux tienen instalado python3, para verificarlo utilice

```bash
$ python3 --version
```

En caso de obtener un error instale python3 siguiendo las instrucciones

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

Además de python necesitaremos pip, al instalar python3 ya lo tendremos disponible, para verificar utilice

```bash
$ pip --version
```
En caso de no tener pip ejecute

```bash
$ sudo apt install python3-pip
```

### Configuración del ambiente virtual

En el dojo se hará uso de los ambientes virtuales de Python, para ello utilizaremos venv. Esta herramienta ya viene con la librería estándar de Python desde la versión 3.3.

Para crear el ambiente virtual, primero creamos un nuevo directorio y luego procedemos a generar el ambiente virtual.

```bash
$ mkdir dojo-django
$ cd dojo-django
$ python3 -m venv ambiente-dojo
```

### Activar el ambiente virtual

Luego debemos activar el ambiente para poder trabajar sobre él. Ésto se hace ejecutando el archivo **activate** en el directorio de Scripts que se generó al crear el ambiente virtual.

```bash
$ source ambiente-dojo/bin/activate
```

Para confirmar que se está haciendo uso del ambiente virtual, puede verificar que el interprete de Python tenga la ruta del ambiente virtual creado.

```bash
$ which python
../ambiente-dojo/bin/python
```

### Instalación de Django

Luego procedemos a la instalación de django dentro del ambiente virtual.

```bash
$ pip install django
```

### Desativar el ambiente virtual

Cuando ya no necesitemos trabajar sobre el ambiente virtual, lo debemos desactivar para evitar confusión en la instalación de librerías.

Para desactivar el ambiente virtual ejecute.

```bash
$ deactivate
```
