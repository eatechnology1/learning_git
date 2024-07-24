# Aprendizaje de Git

<p align="justify">
Bienvenido a mi repositorio de aprendizaje de Git. Aquí documentaré mi progreso y compartiré los comandos básicos que he aprendido. Mi nombre es <strong>Alexander Calderon</strong>, y puedes encontrar más sobre mí y mis servicios en <a href="https://ea-tech.site/">ea-tech.site</a>.
</p>

<p align="center">
    <img src="https://ea-tech.site/wp-content/uploads/2024/07/learnig_git.jpg" alt="Aprendizaje de Git">
</p>


## Introducción

Este repositorio está diseñado para guiarte en el uso de Git desde cero, cubriendo los comandos esenciales y sus usos. Espero que te sea útil en tu camino para dominar Git.

## Comandos Básicos de Git

### Mostrar la Versión de Git
```bash
git --version
```
Verifica la versión de Git instalada en tu sistema.

### Obtener Ayuda
```bash
git help <comando>
```
Proporciona ayuda sobre los comandos de Git.

## Configuración Inicial

### Configurar el Usuario
```bash
git config --global user.name "tu_nombre"
```
Establece tu nombre de usuario global para todos los repositorios.

### Configurar el Correo Electrónico
```bash
git config --global user.email "tu_email@example.com"
```
Establece tu correo electrónico global para todos los repositorios.

### Ver la Configuración Actual
```bash
git config --list
```
Lista la configuración actual de Git.

## Trabajando con Repositorios Locales

### Iniciar un Nuevo Repositorio
```bash
git init
```
Inicializa un nuevo repositorio Git en el directorio actual.

### Ver el Estado de los Archivos
```bash
git status
```
Muestra el estado de los archivos en el repositorio.

### Agregar Archivos al Área de Preparación
```bash
git add --all
```
Agrega todos los archivos pendientes de cambios al área de preparación.

### Agregar Archivos en el Directorio Actual
```bash
git add .
```
Agrega todos los archivos en el directorio actual al área de preparación.

### Confirmar Cambios
```bash
git commit -m "mensaje del commit"
```
Guarda los cambios agregados en el repositorio local con un mensaje descriptivo.

### Modificar el Último Commit
```bash
git commit --amend
```
Abre un editor para modificar el último commit (reemplaza el último commit).

## Trabajando con Tags

### Crear un Tag
```bash
git tag <tag> -m "mensaje del tag"
```
Crea un nuevo tag con un mensaje descriptivo.

### Listar Tags
```bash
git tag
```
Lista todos los tags en el repositorio.

### Borrar un Tag
```bash
git tag -d <tag>
```
Elimina un tag específico.

### Crear un Tag en un Commit Anterior
```bash
git tag -a <tag> <commit> -m "mensaje del tag"
```
Crea un tag anotado en un commit anterior.

### Mostrar Información del Tag
```bash
git show <tag>
```
Muestra información detallada sobre un tag específico.

## Deshaciendo Cambios

### Deshacer el Último Commit (Elimina Cambios del Área de Preparación)
```bash
git reset
```
Deshace el último commit, eliminando los cambios del área de preparación.

### Deshacer el Último Commit (Conserva Cambios en el Área de Preparación)
```bash
git reset --soft
```
Deshace el último commit, conservando los cambios en el área de preparación.

### Cambiar a un Commit Específico (Elimina Todos los Cambios Posteriores)
```bash
git reset --hard <commit>
```
Cambia a un commit específico y elimina todos los cambios posteriores a este.

## Visualización de Historial

### Mostrar el Historial de Commits
```bash
git log --oneline
```
Muestra un historial compacto de los commits.

### Mostrar Historial de Todas las Ramas en Forma Gráfica
```bash
git log --oneline --graph --all
```
Lista todos los commits de todas las ramas de forma gráfica, tomando como base la rama actual.

## Trabajo con Ramas

### Crear una Nueva Rama
```bash
git branch <rama>
```
Crea una nueva rama.

### Listar Ramas
```bash
git branch
```
Muestra en qué rama estás y lista las demás.

### Cambiar a una Rama Específica
```bash
git checkout <rama>
```
Cambia a una rama específica.

### Crear y Cambiar a una Nueva Rama
```bash
git checkout -b <rama>
```
Crea y cambia a una nueva rama.

### Renombrar la Rama Actual
```bash
git branch -m <rama>
```
Renombra la rama actual.

### Eliminar una Rama
```bash
git branch -d <rama>
```
Elimina una rama.

### Fusionar Ramas

#### Hacer un Merge
```bash
git merge <rama>
```
Trae los cambios de la rama especificada a la rama actual.

#### Hacer un Merge sin Fast-Forward
```bash
git merge --no-ff <rama>
```
Junta dos ramas, pero las mantiene. Genera un commit del merge en la rama actual.

### Reorganizar Commits (Rebase)
```bash
git rebase <rama>
```
Trae los commits de otra rama a la rama actual, reorganizando los commits.

## Trabajando con Repositorios Remotos

### Vincular Repositorio Remoto
```bash
git remote add origin <url>
```
Vincula un repositorio remoto con el repositorio local.

### Cambiar URL del Repositorio Remoto
```bash
git remote set-url origin <url>
```
Cambia la URL del repositorio remoto.

### Mostrar Repositorios Remotos
```bash
git remote -v
```
Muestra los repositorios remotos vinculados.

### Subir Cambios al Repositorio Remoto

#### Especificar la Rama Principal
```bash
git push -u origin <rama>
```
Sube los cambios del repositorio local al remoto y especifica la rama principal.

#### Subir Cambios
```bash
git push
```
Sube los cambios del repositorio local al remoto de la rama principal.

#### Subir Cambios de una Rama Específica
```bash
git push origin <rama>
```
Sube los cambios del repositorio local al remoto de una rama específica.

### Eliminar una Rama Remota
```bash
git push origin --delete <rama>
```
Elimina una rama remota.

### Subir Tags
```bash
git push --tags
```
Sube todos los tags locales al remoto.

### Eliminar un Tag Remoto
```bash
git tag -d <tag>
git push origin :refs/tags/<tag>
```
Elimina un tag remoto.

### Sincronizar Cambios con el Repositorio Remoto

#### Descargar y Actualizar la Rama por Defecto
```bash
git pull
```
Descarga los cambios del repositorio remoto y actualiza el local en la rama por defecto.

#### Descargar y Actualizar una Rama Específica
```bash
git pull origin <rama>
```
Descarga los cambios del repositorio remoto y actualiza el local en una rama específica.

### Clonar Repositorios

#### Clonar un Repositorio Remoto
```bash
git clone <url>
```
Clona un repositorio remoto en la rama por defecto.

#### Clonar un Repositorio Remoto en una Rama Específica
```bash
git clone --branch <rama> <url>
```
Clona un repositorio remoto en una rama específica.

