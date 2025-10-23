# Modulo 2

---

## Temario

- [Modulo 2](#modulo-2)
  - [Temario](#temario)
  - [MÓDULO 2: Flujo básico de trabajo en Git](#módulo-2-flujo-básico-de-trabajo-en-git)
    - [Objetivo](#objetivo)
    - [1. Crear un repositorio (`git init`)](#1-crear-un-repositorio-git-init)
    - [2. Clonar un repositorio (`git clone`)](#2-clonar-un-repositorio-git-clone)
    - [3. Agregar archivos (`git add`)](#3-agregar-archivos-git-add)
    - [4. Confirmar cambios (`git commit`)](#4-confirmar-cambios-git-commit)
    - [5. Ver historial (`git log`, `git show`)](#5-ver-historial-git-log-git-show)
      - [Ver todos los commits](#ver-todos-los-commits)
      - [Ver detalles de un commit específico](#ver-detalles-de-un-commit-específico)
    - [6. Ver diferencias (`git diff`)](#6-ver-diferencias-git-diff)
      - [Ver qué ha cambiado desde el último commit](#ver-qué-ha-cambiado-desde-el-último-commit)
      - [Ver diferencias entre commits](#ver-diferencias-entre-commits)
    - [7. Deshacer cambios](#7-deshacer-cambios)
    - [8. Eliminar y renombrar archivos](#8-eliminar-y-renombrar-archivos)
      - [Eliminar archivos del repositorio](#eliminar-archivos-del-repositorio)
      - [Renombrar archivos](#renombrar-archivos)
    - [Flujo completo (resumen visual)](#flujo-completo-resumen-visual)

[Regresar a la nota principal](./../readme.md#módulo-2-flujo-básico-de-trabajo-en-git)

---

## MÓDULO 2: Flujo básico de trabajo en Git

### Objetivo

Aprender el **flujo real de trabajo en Git**, es decir, cómo crear un proyecto, guardar versiones, ver los cambios y corregir errores si algo sale mal.

---

### 1. Crear un repositorio (`git init`)

Cuando empiezas un proyecto desde cero:

``` bash
git init
```

Esto crea una carpeta oculta llamada `.git`, donde se guardará **todo el historial de versiones**.

📁 Estructura:

``` txt
mi-proyecto/
 ┣ .git/      ← Aquí Git guarda los commits, ramas, configuraciones, etc.
 ┗ archivo.txt
```

> ⚠️ No elimines la carpeta `.git` o perderás todo el historial del proyecto.

---

### 2. Clonar un repositorio (`git clone`)

Cuando quieres **copiar un proyecto existente desde GitHub o GitLab**, se usa:

``` bash
git clone https://github.com/usuario/repositorio.git
```

Esto:

- Descarga todos los archivos.
- Trae todo el historial de commits.
- Crea una carpeta local lista para trabajar.

💡 Ejemplo:

``` bash
git clone https://github.com/torvalds/linux.git
```

---

### 3. Agregar archivos (`git add`)

Antes de guardar los cambios, debes **decirle a Git qué archivos quieres incluir** en el siguiente commit.

``` bash
git add archivo.txt
# o para agregar todos los archivos modificados
git add .
```

Esto mueve los archivos al **staging area** (área de preparación).

> “git add” no guarda los cambios todavía, solo los marca para ser guardados en el próximo commit.

---

### 4. Confirmar cambios (`git commit`)

Cuando ya tienes todo listo:

``` bash
git commit -m "Mensaje descriptivo del cambio"
```

Ejemplo:

``` bash
git commit -m "Agregada la función de inicio de sesión"
```

Cada commit:

- Crea una versión del proyecto.
- Guarda la fecha, autor y descripción.
- Te permite volver a ese punto en el futuro.

---

### 5. Ver historial (`git log`, `git show`)

#### Ver todos los commits

``` bash
git log
```

Muestra:

- ID del commit
- Autor
- Fecha
- Mensaje

💡 Versión corta:

``` bash
git log --oneline
```

#### Ver detalles de un commit específico

``` bash
git show <id_del_commit>
```

Ejemplo:

``` bash
git show a3f21b7
```

> Te muestra **qué archivos cambiaron y cómo**.

---

### 6. Ver diferencias (`git diff`)

Sirve para comparar cambios entre versiones o contra el estado actual.

#### Ver qué ha cambiado desde el último commit

``` bash
git diff
```

#### Ver diferencias entre commits

``` bash
git diff <id1> <id2>
```

> 💡 Usa esto antes de hacer un commit para revisar qué vas a guardar.

---

### 7. Deshacer cambios

A veces te equivocas o quieres revertir algo.
Git tiene tres comandos principales para eso: `restore`, `reset` y `checkout`.

**`git restore`:**

Restaura archivos a su estado anterior.

- Deshacer cambios **en el working directory** (sin afectar el historial):

``` bash
git restore archivo.txt
```

- Quitar un archivo del **staging area** (después de `git add`):

``` bash
git restore --staged archivo.txt
```

**`git reset`:**

Sirve para **mover HEAD** (el puntero al último commit) hacia atrás.

Ejemplo:

``` bash
git reset --soft HEAD~1
```

👉 Revierte el último commit, pero mantiene los archivos intactos.

O más fuerte:

``` bash
git reset --hard HEAD~1
```

👉 Revierte el último commit **y borra los cambios del código** también.

> ⚠️ Usa `--hard` con cuidado: los cambios se pierden.

**`git checkout`:**

Permite **moverte entre commits o ramas**.

Ejemplo:

``` bash
git checkout main
```

Cambia a la rama `main`.

O para ver un commit anterior temporalmente:

``` bash
git checkout <id_commit>
```

> Si vuelves a una versión antigua y haces cambios, estarás creando una “línea alternativa” del proyecto.

---

### 8. Eliminar y renombrar archivos

#### Eliminar archivos del repositorio

``` bash
git rm archivo.txt
git commit -m "Archivo eliminado"
```

> Esto elimina el archivo tanto del sistema como del historial de Git.

#### Renombrar archivos

``` bash
git mv viejo.txt nuevo.txt
git commit -m "Archivo renombrado"
```

Git detecta automáticamente el cambio de nombre.

---

### Flujo completo (resumen visual)

``` bash
# 1. Crear o clonar proyecto
git init               # o git clone URL

# 2. Modificar archivos
nano archivo.txt

# 3. Agregar cambios
git add archivo.txt     # o git add .

# 4. Confirmar cambios
git commit -m "Mensaje"

# 5. Revisar historial
git log --oneline

# 6. Si es necesario, deshacer algo
git restore archivo.txt
git reset --hard HEAD~1
```

[Regresar a la nota principal](./../readme.md#módulo-2-flujo-básico-de-trabajo-en-git)

> **Autor:** Fravelz
