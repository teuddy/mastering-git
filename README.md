# Entendiendo Git basico hast avanazado.



## Como guarda Git la data?

Git no trrabaja como los VCS antiguos los cuales almacenaban la informacion en una lista que estaba basada en archivos, es decir que cada vez
que haciamos cambios en el proyecto y guardamos se creaba otro archivo basado en el original con los cambios hechos y asi sucesivamente se creaba una lista de archivos
segun las versiones de nuestro poyecto.

Como Git piensa en sus datos o la manera en la que los guarda es diferente. Cuando guardamos los cambios de nuestro proyecto, **git toma
una foto (snapshot) de como se veia nuestro proyecto en ese entonces y guarda una referencia a ese snapshot**


## El estado de nuestros archivos en Git

Los tres estados de neustros archivos de proyecto en git son:

1) Untracked
2) Unmodified
3) Modified
4) Staged
5) Committed


**Untracked**(Sin rastreo), el archivo cojn este estado **no habia estado en un pasado snapshot**,
por ende git no hace rastreo de este archivo.

**Unmodified**(sin modificar), este archivo estuvo en un snapshot pasado, y  no ha sido modificado.

**Modified**(Modificado), He hecho cambios en un archivo pero no los he entregado (committed) a la base de datos.

**Staged**(Puesto en escena), he marcado que el archivo que modifique ira en mi proxima entrega (commit) a la base de datos.

**Committed**(Entregado), Signfica que los datos de mis archivos han sido guardados en la base de datos local.



## Basicos de Git

Se puede empezar los repositorios de dos maneras:

1) Tomando un directorio local y haciendolo repositorio de Git.
2) Clonar un repositorio Git existente de algun otro lugar.

### Iniciando un repositorio desde un directorio existente

Si se tenemos un directorio donde esta nuestro proyecto y queremos controlarlo con git, primero debemos dirigirnos al directorio.
Esto crea un subdirectorio llamado **.git**, el cual contiene todos los archivos necesitados por el repositorio (esqueleto de repositorio).
*Aun no se esta llevando a cabo ningun rastreo de cambios en archivos*.

Para empezar controlar las versiones de los archivos existentes, debemos empezar a rastrear estos archivos y al final hacer una entrega de estos (commit).
para ellos utilizamos comandos  **add** y luego le hacemos commit, es decir los entregamos.

### Clonando un repositorio existente.

Para cloner un repositorio existente se utiliza **git clone** este comando no solo nso da una copia de la ultima version del proyecto, sino
que nos da toda la data que tiene el servidor, es decir cada version de cada archivo de toda la historia de el repositorio
de ese proyecto.

Ej: git clone https://github.com/libgit2/libgit2 montura (aqui descargamos el repositorio llamado libgit2 en un directorio objetivo 
llamado montura)


## Ingorando archivos 













