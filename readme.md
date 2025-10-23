# Notas-de-Git

Mis notas, y archivos de lectura acerca del funcionamiento de git y github.

---

## TEMARIO COMPLETO DE GIT (BÁSICO → AVANZADO)

---

## Temario

- [Notas-de-Git](#notas-de-git)
  - [TEMARIO COMPLETO DE GIT (BÁSICO → AVANZADO)](#temario-completo-de-git-básico--avanzado)
  - [Temario](#temario)
  - [MÓDULO 1: Introducción a Git](#módulo-1-introducción-a-git)
  - [MÓDULO 2: Flujo básico de trabajo en Git](#módulo-2-flujo-básico-de-trabajo-en-git)
  - [MÓDULO 3: Ramas y fusiones](#módulo-3-ramas-y-fusiones)
  - [MÓDULO 4: Trabajo remoto con GitHub / GitLab](#módulo-4-trabajo-remoto-con-github--gitlab)
  - [MÓDULO 5: Herramientas útiles y comandos avanzados](#módulo-5-herramientas-útiles-y-comandos-avanzados)
  - [MÓDULO 6: Git en entornos reales](#módulo-6-git-en-entornos-reales)
  - [MÓDULO 7: Internals de Git (nivel experto)](#módulo-7-internals-de-git-nivel-experto)
  - [MÓDULO 8: Integración con herramientas externas](#módulo-8-integración-con-herramientas-externas)
  - [BONUS: Recursos y práctica](#bonus-recursos-y-práctica)

---

## MÓDULO 1: Introducción a Git

**Objetivo:** Entender qué es Git, para qué sirve y cómo funciona internamente.

1. ¿Qué es Git y qué problema resuelve?
2. Diferencia entre Git y GitHub/GitLab/Bitbucket.
3. Tipos de control de versiones: local, centralizado y distribuido.
4. Instalación y configuración inicial (`git config`).

   - Configurar nombre y correo.
   - Configurar editor por defecto.
   - Archivo `.gitconfig`.

5. Conceptos clave:

   - Repositorio
   - Commit
   - Branch (rama)
   - Merge (fusión)
   - HEAD
   - Working directory / staging area / repository

Enlace: [Ir a Módulo 1](./modulos/modulo1.md)

---

## MÓDULO 2: Flujo básico de trabajo en Git

**Objetivo:** Aprender el ciclo completo desde crear hasta versionar cambios.

1. Crear un repositorio (`git init`).
2. Clonar un repositorio (`git clone`).
3. Agregar archivos (`git add`).
4. Confirmar cambios (`git commit`).
5. Ver historial (`git log`, `git show`).
6. Ver diferencias (`git diff`).
7. Deshacer cambios:

   - `git restore`
   - `git reset`
   - `git checkout`

8. Eliminar y renombrar archivos (`git rm`, `git mv`).

Enlace: [Ir a Modulo 2](./modulos/modulo2.md)

---

## MÓDULO 3: Ramas y fusiones

**Objetivo:** Dominar el manejo de ramas y la integración de cambios.

1. Crear ramas (`git branch`, `git checkout -b`).
2. Cambiar de rama (`git switch`).
3. Fusionar ramas (`git merge`).
4. Resolver conflictos de merge.
5. Rebases (`git rebase`).
6. Reflog: restaurar cambios perdidos (`git reflog`).
7. Estrategias de branching:

   - Git Flow
   - GitHub Flow
   - Trunk-Based Development

---

## MÓDULO 4: Trabajo remoto con GitHub / GitLab

**Objetivo:** Conectar repositorios locales con repositorios remotos.

1. Conectar un repositorio remoto (`git remote add origin`).
2. Subir cambios (`git push`).
3. Descargar cambios (`git pull`, `git fetch`).
4. Sincronización y conflictos remotos.
5. Autenticación con SSH o HTTPS.
6. Pull requests / merge requests.
7. Forks y contribuciones.
8. Repositorios públicos y privados.

---

## MÓDULO 5: Herramientas útiles y comandos avanzados

**Objetivo:** Aprender herramientas profesionales y comandos potentes.

1. Alias de Git (`git config alias.nombre`).
2. Etiquetas y versiones (`git tag`).
3. Stash: guardar cambios temporales (`git stash`).
4. Cherry-pick: copiar commits específicos (`git cherry-pick`).
5. Bisect: encontrar commits con errores (`git bisect`).
6. Hooks: automatización con scripts (`.git/hooks/`).
7. Submódulos (`git submodule`).
8. Reescribir historial (`git commit --amend`, `git rebase -i`).
9. Limpieza (`git clean`, `git gc`, `.gitignore`).

---

## MÓDULO 6: Git en entornos reales

**Objetivo:** Aplicar Git en proyectos reales, equipos y flujos de trabajo.

1. Buenas prácticas de commits (mensajes claros, convenciones).
2. Convenciones de nombres de ramas.
3. Revisiones de código (code review).
4. Colaboración en proyectos grandes.
5. Integración continua (CI/CD) básica con GitHub Actions / GitLab CI.
6. Backups y recuperación de repositorios.
7. Firmar commits con GPG.
8. Auditoría y seguridad en Git.

---

## MÓDULO 7: Internals de Git (nivel experto)

**Objetivo:** Comprender cómo funciona Git por dentro.

1. Cómo Git guarda los objetos (commits, trees, blobs).
2. Estructura del directorio `.git/`.
3. El archivo `index` y la zona de preparación.
4. Hashing con SHA-1.
5. Refs y HEAD en profundidad.
6. Cómo Git maneja los merges y rebases internamente.
7. Compactación y optimización de datos.
8. Reconstruir un repositorio desde cero.

---

## MÓDULO 8: Integración con herramientas externas

**Objetivo:** Usar Git de forma productiva en distintos entornos.

1. Git con VS Code, Neovim, IntelliJ, etc.
2. Git y entornos de Linux / Windows / macOS.
3. Git en servidores (bare repositories).
4. Git y contenedores (Docker).
5. Git y automatización con scripts bash.

---

## BONUS: Recursos y práctica

**Objetivo:** Perfeccionar tu dominio mediante la práctica constante.

1. Ejercicios prácticos por niveles.
2. Simulación de conflictos y su resolución.
3. Cómo crear tu propio flujo de trabajo profesional.
4. Retos con Git en plataformas como:

   - [learngitbranching.js.org](https://learngitbranching.js.org)
   - [Git Katas](https://github.com/praqma-training/gitkatas)

5. Repositorios para practicar colaboración.

---

**Actualización:** 0.0.2

**Autor:** Fravelz
