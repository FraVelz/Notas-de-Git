
# Modulo 1

[Regresar a la nota principal](./../readme.md#-módulo-1-introducción-a-git)

---

## 🎯 Objetivo

Entender **qué es Git**, **para qué sirve** y **cómo funciona internamente**, para poder usarlo con confianza.

---

## 1. 🧠 ¿Qué es Git y qué problema resuelve?

**Git** es un **sistema de control de versiones**.
Sirve para **guardar los cambios de tu código o proyecto a lo largo del tiempo**, permitiéndote:

* Ver qué cambió y cuándo.
* Volver a versiones anteriores si algo se rompe.
* Trabajar en equipo sin sobrescribir el trabajo de otros.

👉 En otras palabras:
Git **te permite tener un “historial” de tu proyecto**, como una máquina del tiempo.

**Ejemplo:**
Imagina que estás haciendo una app y el día 1 tu código funciona.
El día 2 lo modificas y deja de funcionar 😅
Con Git puedes volver exactamente al código del día 1 con un solo comando.

---

## 2. 🔄 Diferencia entre Git y GitHub / GitLab / Bitbucket

| Herramienta                           | Qué es                                                                                                                    | Dónde se usa                  | Ejemplo                             |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ----------------------------------- |
| **Git**                               | Es el programa que guarda los cambios de tus archivos (control de versiones).                                             | En tu **computador** (local). | `git init`, `git add`, `git commit` |
| **GitHub**, **GitLab**, **Bitbucket** | Son **plataformas online** que guardan tus repositorios Git y te permiten compartirlos, colaborar y hacer copias remotas. | En **Internet** (nube).       | `git push`, `git pull`              |

💡 Piensa así:

> **Git** es el cerebro.
> **GitHub** es la nube donde compartes ese cerebro con otros.

---

## 3. ⚙️ Tipos de control de versiones

| Tipo              | Cómo funciona                                                              | Ejemplo                                  | Desventaja                                                       |
| ----------------- | -------------------------------------------------------------------------- | ---------------------------------------- | ---------------------------------------------------------------- |
| **Local**         | Los cambios solo se guardan en tu propio computador.                       | Git funcionando sin subir nada a GitHub. | Si pierdes tu PC, pierdes el proyecto.                           |
| **Centralizado**  | Todo el trabajo se guarda en un **servidor central**.                      | SVN, CVS.                                | Si el servidor falla, nadie puede trabajar.                      |
| **Distribuido** ✅ | Cada persona tiene una copia **completa del proyecto** (con su historial). | Git.                                     | Puede ser más complejo al inicio, pero es más seguro y flexible. |

📘 Git usa el modelo **distribuido**, por eso cada programador tiene su propia copia con todo el historial del repositorio.

---

## 4. 💻 Instalación y configuración inicial

Una vez instalado Git, debes configurarlo antes de usarlo.

### 🔧 Configurar nombre y correo

Esto identifica quién hace los cambios (commits).

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

> `--global` significa que esta configuración se aplicará para todos los proyectos del computador.

### 📝 Configurar el editor por defecto

```bash
git config --global core.editor "nano"
# O puedes usar "vim", "code --wait" (para VS Code), etc.
```

### 📄 Ver tu configuración actual

```bash
git config --list
```

### 🧩 Archivo `.gitconfig`

Toda esta configuración se guarda en un archivo llamado `.gitconfig`, normalmente en tu carpeta de usuario:

``` txt
~/.gitconfig
```

Puedes abrirlo para ver o editar tus configuraciones.

---

## 5. 🔍 Conceptos clave de Git

### 🧱 Repositorio

Es **la carpeta del proyecto** que Git está controlando.
Se crea con:

```bash
git init
```

Esto genera una carpeta oculta `.git` donde Git guarda **todo el historial**.

---

### 💬 Commit

Un **commit** es como una **foto** o **instantánea** del estado del proyecto en un momento determinado.

👉 Comandos:

```bash
git add archivo.txt   # Marca el archivo para guardar los cambios
git commit -m "Descripción de lo que hiciste"
```

Cada commit guarda:

* Qué cambió
* Cuándo cambió
* Quién lo cambió

---

### 🌿 Branch (rama)

Una **rama** es una **línea paralela de desarrollo**.

* La rama principal se llama `main` o `master`.
* Puedes crear otras ramas para probar cosas sin dañar la principal.

```bash
git branch nueva-rama
git checkout nueva-rama
```

> Así puedes experimentar sin miedo a romper tu código original.

---

### 🔗 Merge (fusión)

**Merge** une los cambios de una rama con otra.

Por ejemplo:

```bash
git checkout main
git merge nueva-rama
```

> Así mezclas los cambios que hiciste en `nueva-rama` dentro de `main`.

---

### 🎯 HEAD

**HEAD** apunta al **último commit actual** o a la rama en la que estás trabajando.

> Piensa en HEAD como el “marcador” que indica **dónde estás parado** en el historial.

```bash
git show HEAD
```

---

### 📂 Working directory / Staging area / Repository

| Zona                     | Qué contiene                                     | Comando relacionado     |
| ------------------------ | ------------------------------------------------ | ----------------------- |
| **Working directory**    | Archivos de tu carpeta actual.                   | `git status`, `git add` |
| **Staging area (index)** | Archivos listos para ser guardados en un commit. | `git add`               |
| **Repository (.git)**    | Donde Git guarda los commits confirmados.        | `git commit`            |

🔁 Flujo típico:

``` txt
Working directory → git add → Staging area → git commit → Repository
```

[Regresar a la nota principal](./../readme.md#-módulo-1-introducción-a-git)

> **Autor:** Fravelz
