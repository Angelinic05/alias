# Taller Alias Git

1. Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es utilizar el comando git log con algunas opciones específicas para obtener un resumen gráfico de los últimos 5 commits en todas las ramas.

   **git config alias.an "log --all --graph --oneline -n 5"**

   **git an**

   - `git config`: Este comando se utiliza para configurar opciones de Git. En este caso, estamos configurando un alias.

   - `alias.an`: Estamos asignando un alias llamado `an` 

     paso a paso:

     - `log`: Indica que queremos ver el registro de commits.
     - `--all`: Muestra commits de todas las ramas.
     - `--graph`: Muestra una representación gráfica del historial de commits.
     - `--oneline`: Muestra cada commit en una línea.
     - `-n 5`: Limita la salida a los últimos 5 commits.

2. Esta trabajando en un proyecto Git colaborativo y necesitas obtener una visión gráfica y detallada del historial de commits. Tu tarea es utilizar el comando git log con opciones específicas para personalizar el formato y presentación de la salida. La salida debe tener las siguientes especificaciones:

   - Muestra una representación gráfica del historial de commits.
   - Muestra el hash corto del commit en color rojo.
   - Muestra las referencias (ramas o tags) en las que está involucrado el commit en color
     amarillo.
   - Muestra el mensaje del commit.
   - Muestra la fecha relativa del commit en color verde.
   - Muestra el hash del commit como un identificador abreviado.
   - Muestra las fechas de los commits de forma relativa.

​			**git config  alias.ge "log --graph --abbrev-commit --decorate --format=format:'%C(red)%h%C(reset) %C(yellow)%d%C(reset) 	%C(white)%s%C(reset) %C(green) (%ar)%C(reset)' --all"**



- `git config`: Como en el caso anterior, se utiliza para configurar opciones de Git.

- `alias.ge`: Se asigna un alias llamado `ge`.

  paso a paso:

  - `log --graph`: Muestra un gráfico del historial de commits.

  - `--abbrev-commit`: Muestra el hash del commit como un identificador abreviado.

  - `--decorate`: Muestra las referencias (ramas o tags) en las que está involucrado el commit.

  - `--format=format:'...'`: Personaliza el formato de salida del log.

  - `%C(color)` y `%C(reset)`: Son secuencias de formato que cambian el color del texto en la salida del log.

  - `%h`: Muestra el hash corto del commit.

  - `%d`: Muestra las referencias (ramas o tags) en las que está involucrado el commit.

  - `%s`: Muestra el mensaje del commit.

  - `%ar`: Muestra la fecha relativa del commit.

  - `%C(red)`, `%C(yellow)`, `%C(white)`, `%C(green)`: Especifica el color del texto.

    

3. Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
   el último commit en la rama actual. Sin embargo, encuentras que escribir este comando
   completo es un poco tedioso. 

   - Tu tarea es utilizar el comando git config para crear un alias llamado last que represente el
     comando git log -1 HEAD.

     **git config --global alias.last "log -1 HEAD"**

     - `git config`: Se utiliza para configurar opciones de Git.

     - `alias.last`: Se asigna un alias llamado `last`.

        paso a paso:

       - `log`: Indica que queremos ver el registro de commits.
       - `-1`: Muestra solo el último commit.
       - `HEAD`: Especifica que queremos el último commit en la rama actual.

4. magina que deseas simplificar el proceso de editar la configuración global de Git. Tu tarea es utilizar el comando git config para crear un alias que te permita abrir fácilmente la configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias llamado ec que cumpla con la especificación dada.

​	**git config --global alias.ec "config --global -e"**

​	

- `git config`: Este comando se utiliza para configurar opciones de Git.

- `--global`: Esta opción indica que la configuración se aplicará a nivel global para todos los repositorios de Git en tu sistema.

- `alias.ec`: Estás creando un alias llamado `ec`.

  paso a paso:

  - `config`: Se refiere al comando `git config`.

  - `--global`: Indica que estamos configurando opciones a nivel global.

  - `-e`: Especifica que queremos abrir el archivo de configuración global de Git en un editor de texto.

    

5. Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores y ramas. Tu tarea es utilizar el comando git log con opciones específicas para personalizar la salida del historial de commits y resaltar información clave. El resultado de la ejecución del comando se debe ve como el ejemplo siguiente:

   **git config  alias.ld "log --graph --abbrev-commit --decorate --format=format:'%C(bold yellow)%h%C(reset)  %C(red)%d%C(reset) %C(red)\ %C(white)%s%C(reset) %C(blue)\ %C(blue)[ %C(blue)%an%C(reset) %C(blue)]' --all"**

   

   1. **`git config`:** Este es el comando principal que se utiliza para configurar opciones de Git.

   2. **`--global`:** Esta opción se utiliza para aplicar la configuración a nivel global en tu sistema, lo que significa que afectará a todos los repositorios de Git en tu máquina.

   3. **`alias.ld`:** Aquí estás creando un alias llamado `ld`, que se utilizará como una abreviatura para el comando `git log` con opciones específicas.

   4. **`"log --graph --abbrev-commit --decorate --format=format:'...' --all"`:**

      - **`log`:** Indica que queremos ver el registro de commits.

      - **`--graph`:** Muestra una representación gráfica del historial de commits.

      - **`--abbrev-commit`:** Muestra el hash del commit como un identificador abreviado.

      - **`--decorate`:** Muestra las referencias (ramas o tags) en las que está involucrado el commit.

      - `--format=format:'...'`:

         Personaliza el formato de salida del log.

        - **`%C(bold yellow)%h%C(reset)`:** Formato para mostrar el hash del commit en negrita y color amarillo.
        - **`%C(red)%d%C(reset)`:** Formato para mostrar las referencias (ramas o tags) en color rojo.
        - **`%C(red)\`:** Inserta un backslash en color rojo.
        - **`%C(white)%s%C(reset)`:** Formato para mostrar el mensaje del commit en color blanco.
        - **`%C(blue)\`:** Inserta un backslash en color azul.
        - **`%C(blue)[ %C(blue)%an%C(reset) %C(blue)]`:** Formato para mostrar el nombre del autor del commit entre corchetes y en color azul.