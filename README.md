# Entendiendo Git basico hasta avanazado.



## 1 **Basico de Git**

### 1.0 Como guarda Git la data?

Git no trrabaja como los VCS antiguos los cuales almacenaban la informacion en una lista que estaba basada en archivos, es decir que cada vez
que haciamos cambios en el proyecto y guardamos se creaba otro archivo basado en el original con los cambios hechos y asi sucesivamente se creaba una lista de archivos
segun las versiones de nuestro poyecto.

Como Git piensa en sus datos o la manera en la que los guarda es diferente. Cuando guardamos los cambios de nuestro proyecto, **git toma
una foto (snapshot) de como se veia nuestro proyecto en ese entonces y guarda una referencia a ese snapshot**


### 1.2 El estado de nuestros archivos en Git

Los tres estados de neustros archivos de proyecto en git son:
1) Modified
2) Staged
3) Committed

**Modified**(Modificado), He hecho cambios en un archivo pero no los he entregado (committed) a la base de datos.

**Staged**(Puesto en escena), he marcado que el archivo que modifique ira en mi proxima entrega (commit) a la base de datos.

**Committed**(Entregado), Signfica que los datos de mis archivos han sido guardados en la base de datos local.

### 1.3 Iniciar repositorio local.

Se puede empezar los repositorios de dos maneras:

1) Tomando un directorio local y haciendolo repositorio de Git.
2) Clonar un repositorio Git existente de algun otro lugar.

Iniciando un repositorio desde un directorio existente

Si se tenemos un directorio donde esta nuestro proyecto y queremos controlarlo con git, primero debemos dirigirnos al directorio.
Esto crea un subdirectorio llamado **.git**, el cual contiene todos los archivos necesitados por el repositorio (esqueleto de repositorio).
*Aun no se esta llevando a cabo ningun rastreo de cambios en archivos*.

Para empezar controlar las versiones de los archivos existentes, debemos empezar a rastrear estos archivos y al final hacer una entrega de estos (commit).
para ellos utilizamos comandos  **add** y luego le hacemos commit, es decir los entregamos.

 Clonando un repositorio existente.

Para cloner un repositorio existente se utiliza **git clone** este comando no solo nso da una copia de la ultima version del proyecto, sino
que nos da toda la data que tiene el servidor, es decir cada version de cada archivo de toda la historia de el repositorio
de ese proyecto.

Ej: git clone https://github.com/libgit2/libgit2 montura (aqui descargamos el repositorio llamado libgit2 en un directorio objetivo 
llamado montura)





## Ingorando archivos 


Hacemos que git ignore archivos que no queremos que trackee, ni que nos aparezca como untracked. Para ellos creamos un archivo llamado
**.gitignore**, dentro colocamos lo que queremos que ignore, para ello debemos seguir ciertos patrones, ej:

**utilizamos (*) para ignorar todos los archivos que cumplan ciertos requisitos , como por ejemplo:**

1) *.[o] , significa "ignora todos los archivos los cuales terminan en la letra o"
2) *.txt, significa "ignora todos los archivos con extension txt"
3) *~, significa "ignora todos los aarchivos que terminen con el simbolo (~).


**utilizamos (/) lo utilizamos para ignorar *pathnames* relativos al gitignore, es decir que esten en el mismo directorio
(no subdirectirio)**
1) /node_modules, "ignora a el archivo con el pathname node_modules"
2) src/*.txt, "ignora todos los txt de src/txt, pero no aquellos que esten en src/server/txt" 
3) doc/* */* .pdf, "ignora los archivos en el directorio doc y los subdirectorios de este que tengan extension .pdf"

**Y si queremos que elimine el archivo de todos los subdirectorios pues lo hacemos de forma recursiva**
1) node_modules/ , "esto eliminara a el archivo no solo de el directorio recurrente sino de los subdirectorios"


**utilizamos (!) para negar cierto pattern**
1) si ignoramos todos los archivos que sean txt ( *.txt ) pero queremos que cierto archivo txt
no sea ignorado, para ello hacemos ( !hello.txt ), de esta manera sobreescribimos el otro pattern.


