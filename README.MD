# Guia de comandos Git en español
###### MAURICIO NUÑEZ
------------
### Requisitos minimos. <br>
Git instalado <br>
Terminal bash  (Git instala una por defecto) <br>
comandos basicos bash <br>


##### Conceptos basicos <br>

<font size="1">

**Flujo / Flow:**  
El flujo de trabajo en Git se refiere a cómo se estructuran y gestionan las operaciones de control de versiones para colaborar de manera consistente y productiva.

**Rama / Branch:**  
Una rama en Git es una línea de desarrollo independiente que permite trabajar en características o correcciones sin afectar directamente la rama principal del proyecto.

**Funcionalidad / Feature:**  
Una funcionalidad es una mejora específica desarrollada en una rama separada para facilitar el desarrollo paralelo y la gestión de cambios, luego se fusiona con la rama principal.

**Integración / Integration:**  
La integración en Git se refiere a combinar cambios de diferentes ramas o colaboradores en la rama principal, asegurando la consolidación y disponibilidad de todas las funcionalidades y correcciones en la versión principal del software.

</font>

## Comandos Git <br>

Una vez abierta nuestra terminal de preferencia tenemos el siguiente abanico de comandos <br>

| Comando | Utilidad | Descripción |
|---------|-------------|-------------|
|`git config --global user.name "nombre de usuario"`| Configuración inicial | [Detalles](#descripcion-config-usuario) |
| `git config --global user.email "email asociado a git"` | Configuración inicial | [Detalles](#descripcion-config-email) |
| `git init` | Iniciar un nuevo repositorio | [Detalles](#descripcion-init) |
| `git config --global init.defaultBranch main` | Configurar rama predeterminada | [Detalles](#descripcion-config-default-branch) |
| `git branch -m main` | Cambiar nombre de la rama principal | [Detalles](#descripcion-branch-m) |
| `git status` | Verificar estado de los archivos | [Detalles](#descripcion-status) |
| `git add nombre del archivo` | Agregar archivo al área de preparación | [Detalles](#descripcion-add) |
| `git add .` | Agregar todos los archivos al área de preparación | [Detalles](#descripcion-add-all) |
| `git commit -m  "mensaje o comentario del commit"`| Confirmar cambios con mensaje | [Detalles](#descripcion-commit) |
| `git checkout nombre_del_fichero o id de fichero` | Cambiar entre ramas o versiones de archivos | [Detalles](#descripcion-checkout) |
| `git reset` | Deshacer cambios locales | [Detalles](#descripcion-reset) |
| `git log --graph --decorate --all --oneline` | Visualizar historial de commits de manera gráfica | [Detalles](#descripcion-log-graph) |
| `git config --global alias.nombre de alias "comando de git "` | Crear alias para comandos frecuentes | [Detalles](#descripcion-alias) |
| `git ignore` | Especificar archivos a ignorar | [Detalles](#descripcion-ignore) |
| `git diff` | Ver diferencias entre cambios | [Detalles](#descripcion-diff) |
| `git reflog` | Registrar referencias de HEAD | [Detalles](#descripcion-reflog) |
| `git tag nombre_tag_deseado` | Etiquetar un commit | [Detalles](#descripcion-tag) |
| ` git tag` | Ver y listar tags existentes | [Detalles](#descripcion-list-tag) |
| `git checkout tags/nombre_tag` | Cambiar a un tag específico | [Detalles](#descripcion-checkout-tag) |
| `git branch nombre_de_rama_nueva` | Crear una nueva rama | [Detalles](#descripcion-branch) |
| `git branch` | Ver lista de ramas | [Detalles](#descripcion-branch-list) |
| `git switch nombre_de_rama` | Cambiar a una rama existente | [Detalles](#descripcion-switch) |
| `git merge` | Fusionar cambios de una rama a otra | [Detalles](#descripcion-merge) |
| `git stash` | Guardar cambios sin realizar un commit | [Detalles](#descripcion-stash) |
| `git stash pop` | Recuperar cambios guardados con stash | [Detalles](#descripcion-stash-pop) |
| `git branch -d nombre de rama` | Eliminar una rama | [Detalles](#descripcion-branch-delete) |
| `git clone url o ssh` | Clonar un repositorio remoto | [Detalles](#descripcion-clone) |
| `git push origin nombre_de_rama` | Enviar cambios a un repositorio remoto | [Detalles](#descripcion-push) |
| `git fetch` | Obtener cambios del repositorio remoto | [Detalles](#descripcion-fetch) |
| `git pull origin nombre_de_rama` | Obtener y fusionar cambios del repositorio remoto | [Detalles](#descripcion-pull) |
| `git clone` | Clonar un repositorio remoto | [Detalles](#descripcion-clone) |




<a name="descripcion-config-usuario"></a>

## Configuración de Usuario
El comando git config --global user.name "nombre de usuario" se utiliza para establecer el nombre de usuario asociado con los commits de Git a nivel global. Esto es esencial para identificar quién realizó un cambio en el repositorio. Este comando establece la configuración global, lo que significa que se aplicará a todos los repositorios Git en tu sistema.

<a name="descripcion-config-email"></a>

## Configuración de Correo Electrónico
El comando git config --global user.email "email asociado a git" se utiliza para configurar la dirección de correo electrónico asociada con los commits de Git a nivel global. Similar a la configuración de nombre de usuario, la configuración de correo electrónico es crucial para la identificación del autor de un cambio. Al establecerlo globalmente, se aplica a todos los repositorios Git en tu sistema.

<a name="descripcion-init"></a>

## Iniciar un Nuevo Repositorio
El comando git init es el primer paso para comenzar a utilizar Git en un proyecto. Cuando ejecutas este comando en un directorio, Git inicializa un nuevo repositorio en ese directorio, creando una estructura interna que le permite realizar un seguimiento de los cambios en tu proyecto.

<a name="descripcion-config-default-branch"></a>

## Configurar Rama Predeterminada
El comando git config --global init.defaultBranch main establece la rama predeterminada para los nuevos repositorios. Esto es útil si prefieres utilizar un nombre diferente a la convención estándar "master" para la rama principal de tu repositorio. Al establecerlo globalmente, afectará a todos los repositorios nuevos.

<a name="descripcion-branch-m"></a>

## Cambiar Nombre de la Rama Principal
El comando git branch -m main te permite cambiar el nombre de la rama principal de tu repositorio. Esto puede ser útil si estás adoptando una convención de nomenclatura diferente o si deseas reflejar cambios en la estructura de ramificación de tu proyecto.

<a name="descripcion-status"></a>

## Verificar Estado de los Archivos
El comando git status es una herramienta esencial para entender el estado actual de tu repositorio. Muestra información sobre los cambios pendientes, archivos no seguimientos y la rama actual. Puede ayudarte a determinar qué archivos están listos para ser comprometidos y qué cambios necesitan ser agregados al área de preparación.

<a name="descripcion-add"></a>

## Agregar Archivo al Área de Preparación
El comando git add nombre del archivo añade un archivo específico al área de preparación, también conocida como "staging area". Los archivos en el área de preparación están listos para ser incluidos en el próximo commit. Este comando es esencial para seleccionar de manera precisa los cambios que deseas incluir en cada commit.

<a name="descripcion-add-all"></a>

## Agregar Todos los Archivos al Área de Preparación
El comando git add . es una forma conveniente de agregar todos los archivos modificados al área de preparación. Esto es útil cuando has realizado cambios en varios archivos y deseas incluir todos estos cambios en el próximo commit.

<a name="descripcion-commit"></a>

##  Confirmar Cambios con Mensaje
El comando git commit -m "mensaje o comentario del commit" realiza un commit con los archivos que están en el área de preparación. Este comando captura un punto en la historia del proyecto y requiere un mensaje descriptivo que explique los cambios realizados. Proporcionar mensajes claros y concisos es una buena práctica para mantener un historial de cambios comprensible.

<a name="descripcion-checkout"></a>

## Cambiar Entre Ramas o Versiones de Archivos
El comando git checkout nombre_del_fichero o id de fichero te permite cambiar entre ramas o versiones específicas de archivos. Puedes utilizar este comando para explorar diferentes estados de tu proyecto sin comprometer los cambios actuales.

<a name="descripcion-reset"></a>

## Deshacer Cambios Locales
El comando git reset deshace los cambios locales en el directorio de trabajo. Puedes utilizarlo para eliminar cambios no deseados en el área de preparación o para revertir cambios confirmados en el historial.

<a name="descripcion-log-graph"></a>

## Visualizar Historial de Commits de Manera Gráfica
El comando git log --graph --decorate --all --oneline proporciona una representación gráfica del historial de commits. Esto incluye información sobre las ramas, las fusiones y los commits individuales. Es una herramienta útil para visualizar la estructura del historial del proyecto.

<a name="descripcion-alias"></a>

## Crear Alias para Comandos Frecuentes
El comando git config --global alias.nombre de alias "comando de git " permite crear alias para comandos Git frecuentemente utilizados. Los alias son atajos que simplifican la ejecución de comandos largos y complejos.

<a name="descripcion-ignore"></a>

## Especificar Archivos a Ignorar
El comando git ignore se utiliza para especificar patrones de archivos que Git debe ignorar. Puedes configurar este archivo para evitar que archivos específicos o patrones de archivos se incluyan en el seguimiento de Git.

<a name="descripcion-diff"></a>

## Ver Diferencias Entre Cambios
El comando git diff muestra las diferencias entre los cambios realizados en el directorio de trabajo y el último commit. Puedes utilizarlo para revisar los cambios antes de realizar un commit.

<a name="descripcion-reflog"></a>

## Registrar Referencias de HEAD
El comando git reflog muestra un registro de todas las acciones realizadas en el repositorio, incluyendo cambios de rama, fusiones y commits. Es útil para retroceder a estados anteriores del proyecto.

<a name="descripcion-tag"></a>

## Etiquetar un Commit
El comando git tag nombre_tag_deseado crea una etiqueta para marcar un commit específico. Las etiquetas son útiles para identificar versiones importantes o hitos en el desarrollo del proyecto.

<a name="descripcion-list-tag"></a>

## Ver y Listar Tags Existentes
El comando git tag muestra la lista de tags existentes en el repositorio. Puedes utilizarlo para verificar las etiquetas disponibles y sus nombres.

<a name="descripcion-checkout-tag"></a>

## Cambiar a un Tag Específico
El comando git checkout tags/nombre_tag te permite cambiar al estado representado por un tag específico. Esto puede ser útil para revisar el código en un estado específico del proyecto.

<a name="descripcion-branch"></a>

## Crear una Nueva Rama
El comando git branch nombre_de_rama_nueva crea una nueva rama en el repositorio. Las ramas son utilizadas para desarrollar funcionalidades de manera independiente o para aislar cambios experimentales.

<a name="descripcion-branch-list"></a>

## Ver Lista de Ramas
El comando git branch muestra la lista de ramas en el repositorio. Puedes utilizarlo para verificar qué ramas existen y cuál es la rama actual.

<a name="descripcion-switch"></a>

## Cambiar a una Rama Existente
El comando git switch nombre_de_rama te permite cambiar al estado representado por una rama específica. Esto cambia tu directorio de trabajo y el índice al estado de la rama seleccionada.

<a name="descripcion-merge"></a>

## Fusionar Cambios de una Rama a Otra
El comando git merge fusiona los cambios de una rama en otra. Es una operación común cuando trabajas en equipo y necesitas combinar el trabajo realizado en diferentes ramas.

<a name="descripcion-stash"></a>

## Guardar Cambios sin Realizar un Commit
El comando git stash guarda temporalmente los cambios en un stash para aplicarlos más tarde. Puedes utilizarlo cuando necesitas cambiar de rama o de estado sin comprometer los cambios actuales.

<a name="descripcion-stash-pop"></a>

## Recuperar Cambios Guardados con Stash
El comando git stash pop recupera los cambios guardados en un stash y los aplica en el directorio de trabajo. Es útil cuando deseas reintegrar cambios guardados previamente.

<a name="descripcion-branch-delete"></a>

## Eliminar una Rama
El comando git branch -d nombre de rama elimina una rama específica en el repositorio. Antes de eliminar una rama, asegúrate de haber fusionado los cambios necesarios.

<a name="descripcion-clone"></a>

## Clonar un Repositorio Remoto
El comando git clone url o ssh clona un repositorio remoto en el directorio actual. Esto crea una copia completa del repositorio, incluyendo todas las ramas y la historia de commits.

<a name="descripcion-push"></a>

## Enviar Cambios a un Repositorio Remoto
El comando git push origin nombre_de_rama envía los cambios locales a un repositorio remoto en una rama específica. Es fundamental para compartir tu trabajo con otros colaboradores.

<a name="descripcion-fetch"></a>

## Obtener Cambios del Repositorio Remoto
El comando git fetch obtiene los cambios del repositorio remoto sin fusionarlos en el repositorio local. Es útil para revisar los cambios antes de fusionarlos.

<a name="descripcion-pull"></a>

## Obtener y Fusionar Cambios del Repositorio Remoto
El comando git pull origin nombre_de_rama obtiene y fusiona los cambios del repositorio remoto en el repositorio local. Simplifica el proceso de obtener y aplicar los cambios más recientes.
 
a
