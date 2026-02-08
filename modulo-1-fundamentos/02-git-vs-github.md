# 1.2 - Diferencias entre Git y GitHub

## 📋 Objetivos de Aprendizaje

- Distinguir claramente entre Git y GitHub
- Comprender el rol de cada herramienta en el desarrollo
- Conocer alternativas a GitHub
- Entender cómo trabajan juntos Git y GitHub
- Identificar cuándo usar uno u otro

## 📚 Contenido

### Introducción

Una confusión muy común, especialmente entre principiantes, es pensar que Git y GitHub son lo mismo. **¡No lo son!** Aunque trabajan juntos perfectamente, son herramientas completamente diferentes con propósitos distintos.

### ¿Qué es Git?

**Git** es un **sistema de control de versiones distribuido** creado por Linus Torvalds en 2005.

```
Git = Software de Control de Versiones
```

#### Características de Git:

✅ **Software libre y open source**
- Completamente gratis
- Código abierto
- Multiplataforma (Windows, Mac, Linux)

✅ **Local**
- Se instala en tu computadora
- No necesita internet para funcionar
- Trabaja con tu sistema de archivos

✅ **Línea de comandos**
- Principalmente se usa desde la terminal
- Existen interfaces gráficas opcionales
- Comandos poderosos y flexibles

✅ **Distribuido**
- Cada desarrollador tiene el repositorio completo
- No depende de un servidor central
- Puede funcionar completamente offline

#### ¿Qué hace Git?

```bash
# Crea repositorios
git init

# Rastrea cambios
git add archivo.js
git commit -m "Mensaje"

# Gestiona ramas
git branch feature-nueva
git checkout feature-nueva

# Combina cambios
git merge feature-nueva

# Y mucho más...
```

#### Analogía de Git

Piensa en Git como un **diario fotográfico inteligente** de tu proyecto:
- Cada "foto" (commit) captura el estado completo
- Puedes volver a cualquier "foto" anterior
- Puedes tener "álbumes paralelos" (branches)
- Todo está en tu computadora (local)

### ¿Qué es GitHub?

**GitHub** es una **plataforma de alojamiento web** para repositorios Git, creada en 2008 (adquirida por Microsoft en 2018).

```
GitHub = Servicio Web + Red Social para Código
```

#### Características de GitHub:

✅ **Servicio en la nube**
- Aloja repositorios Git online
- Accesible desde cualquier lugar
- Respaldo automático en la nube

✅ **Colaboración**
- Pull Requests para code review
- Issues para seguimiento de tareas
- Discussions para comunicación
- Projects para gestión de proyectos

✅ **Herramientas adicionales**
- GitHub Actions (CI/CD)
- GitHub Pages (hosting estático)
- GitHub Packages (registro de paquetes)
- Seguridad y análisis de código

✅ **Red social para desarrolladores**
- Perfiles públicos
- Seguir proyectos y personas
- Contribuir a proyectos open source
- Mostrar tu portafolio

#### ¿Qué hace GitHub?

```
📦 Aloja repositorios Git en la nube
👥 Facilita la colaboración en equipo
🔄 Gestiona Pull Requests y Code Review
📊 Proporciona herramientas de gestión de proyectos
🚀 Automatiza con CI/CD
🌐 Publica sitios web con GitHub Pages
```

#### Analogía de GitHub

Piensa en GitHub como **Google Drive o Dropbox, pero especializado para código**:
- Sube tu "diario fotográfico" (repositorio Git) a la nube
- Otros pueden ver, comentar y contribuir
- Incluye herramientas colaborativas avanzadas
- Es la "red social" donde vive el código

### Comparación Directa

| Aspecto | Git | GitHub |
|---------|-----|--------|
| **Tipo** | Software | Servicio Web |
| **Creación** | 2005 (Linus Torvalds) | 2008 (Tom Preston-Werner) |
| **Costo** | Gratis | Gratis + Planes pagos |
| **Ubicación** | Local (tu PC) | Nube (servidores) |
| **Funciona sin internet** | ✅ Sí | ❌ No |
| **Instalación** | Se instala | Cuenta web |
| **Función principal** | Control de versiones | Alojamiento + Colaboración |
| **Interfaz** | CLI (terminal) | Web + CLI opcional |
| **Colaboración** | Básica | Avanzada |
| **Herramientas extras** | Ninguna | Actions, Pages, Projects, etc. |

### Cómo Trabajan Juntos

```
Tu Computadora (Git)          →          GitHub (Nube)
─────────────────────                    ──────────────
1. Haces cambios                         
2. git add                               
3. git commit                            
4. git push                      →       Repositorio remoto
5. git pull                      ←       Cambios de otros
```

#### Flujo Típico:

```bash
# 1. Git local: trabajas en tu código
git add archivo.js
git commit -m "Nueva característica"

# 2. Git + GitHub: sincronizas con la nube
git push origin main

# 3. GitHub: otros ven tus cambios, abren PRs, comentan

# 4. Git local: descargas cambios de otros
git pull origin main
```

### Git puede vivir sin GitHub

Git es **completamente independiente**. Puedes usar Git sin GitHub:

```bash
# Repositorio Git totalmente local
git init mi-proyecto
cd mi-proyecto
git add .
git commit -m "Primer commit"

# ✅ Ya tienes control de versiones
# ❌ No hay colaboración online
# ❌ No hay respaldo en la nube
```

### GitHub necesita Git

GitHub está **construido sobre Git**. No puedes usar GitHub sin entender Git:

- Los repositorios en GitHub son repositorios Git
- Los comandos de sincronización usan Git
- La lógica de branches, commits, merges es de Git

### Alternativas a GitHub

Git puede trabajar con muchas plataformas, no solo GitHub:

#### **GitLab**
```
✅ Similar a GitHub
✅ CI/CD integrado robusto
✅ Self-hosted disponible
✅ Muy usado en empresas
```

#### **Bitbucket**
```
✅ Integración con Atlassian (Jira, Confluence)
✅ Popular en empresas
✅ Repositorios privados ilimitados
```

#### **Gitea**
```
✅ Ligero y rápido
✅ Self-hosted
✅ Open source
✅ Para servidores propios
```

#### **Azure DevOps**
```
✅ Microsoft
✅ Integración con Azure
✅ Herramientas enterprise completas
```

#### Sin plataforma (solo Git)
```bash
# Servidor Git propio
ssh usuario@servidor
cd /var/git/proyecto.git
git init --bare

# Todos clonanan de ahí
git clone ssh://usuario@servidor/var/git/proyecto.git
```

### Qué Puedes Hacer Solo con Git

✅ Control de versiones completo
✅ Branches y merges
✅ Historial y reversión
✅ Trabajo offline
✅ Repositorios locales
✅ Compartir por email/USB (no recomendado)

### Qué Necesitas GitHub (u otra plataforma)

✅ Colaboración online
✅ Respaldo en la nube
✅ Pull Requests y Code Review
✅ Issues y gestión de proyectos
✅ CI/CD automatizado
✅ GitHub Pages para sitios web
✅ Visibilidad y portafolio público
✅ Contribuciones a proyectos open source

### Casos de Uso

#### Solo Git (Local)
```
📝 Proyecto personal simple
💻 Experimentos y aprendizaje
📚 Control de versiones de documentos
🔒 Proyectos ultra confidenciales (sin nube)
```

#### Git + GitHub
```
👥 Proyectos en equipo
🌍 Proyectos open source
💼 Portafolio profesional
🚀 Proyectos con CI/CD
📊 Proyectos que necesitan gestión avanzada
```

### Errores Comunes

❌ **"Voy a aprender GitHub primero, luego Git"**
✅ Debes aprender Git primero. GitHub se construye sobre Git.

❌ **"Git y GitHub son lo mismo"**
✅ Git es el motor, GitHub es la plataforma que lo usa.

❌ **"No necesito aprender Git, solo usaré GitHub Desktop"**
✅ Las interfaces gráficas ayudan, pero necesitas entender Git.

❌ **"Si uso GitLab, no necesito aprender Git"**
✅ Todas las plataformas usan Git internamente.

### Visualización de la Relación

```
┌─────────────────────────────────────────┐
│                                         │
│  GIT (El Motor)                         │
│  ────────────────                       │
│  • Sistema de control de versiones      │
│  • Local                                │
│  • Línea de comandos                    │
│  • Independiente                        │
│                                         │
│         ↓ usado por ↓                   │
│                                         │
│  GITHUB (La Plataforma)                 │
│  ───────────────────                    │
│  • Servicio web                         │
│  • Colaboración                         │
│  • Herramientas extras                  │
│  • Depende de Git                       │
│                                         │
└─────────────────────────────────────────┘
```

### Analogía Final

**Git** es como el **motor de un auto**:
- Funciona independientemente
- Potente y confiable
- Puedes usarlo solo

**GitHub** es como una **autopista con servicios**:
- Facilita el viaje
- Agrega comodidades
- Conecta con otros
- Pero necesitas el motor (Git) para usarla

## 🧪 Ejercicios Prácticos

### Ejercicio 1: Identificación
**Objetivo:** Distinguir entre Git y GitHub

**Lee las siguientes afirmaciones e identifica si hablan de Git o GitHub:**

1. "Instalé esto en mi computadora" → ?
2. "Creé mi cuenta y ahora tengo un perfil público" → ?
3. "Funciona sin conexión a internet" → ?
4. "Abrí un Pull Request para mi código" → ?
5. "Usé `git commit` para guardar cambios" → ?
6. "Configuré GitHub Actions para CI/CD" → ?
7. "Es software libre creado por Linus Torvalds" → ?
8. "Microsoft lo compró en 2018" → ?

**Respuestas:** 1-Git, 2-GitHub, 3-Git, 4-GitHub, 5-Git, 6-GitHub, 7-Git, 8-GitHub

### Ejercicio 2: Escenarios
**Objetivo:** Identificar cuándo necesitas cada herramienta

**Para cada escenario, indica si necesitas solo Git, o Git + GitHub:**

1. Control de versiones de tu proyecto personal offline
2. Colaborar con un equipo de 10 personas
3. Crear tu portafolio de desarrollador público
4. Contribuir a un proyecto open source
5. Practicar comandos de Git en tu laptop
6. Automatizar tests cada vez que subes código

### Ejercicio 3: Investigación
**Objetivo:** Conocer el ecosistema

**Investiga y compara:**
1. Busca 2 alternativas a GitHub
2. Compara características principales
3. Identifica cuál es más popular en tu país/industria
4. ¿Cuál usarías y por qué?

## ✅ Checklist de Aprendizaje

- [ ] Entiendo que Git y GitHub son cosas diferentes
- [ ] Sé que Git es software y GitHub es servicio web
- [ ] Comprendo que Git puede funcionar sin GitHub
- [ ] Identifico que GitHub necesita Git para funcionar
- [ ] Conozco alternativas a GitHub
- [ ] Puedo explicar cuándo usar solo Git vs Git + GitHub
- [ ] Entiendo cómo trabajan juntos

## 🔍 Recursos Adicionales

- [Git Official Site](https://git-scm.com/)
- [GitHub Official Site](https://github.com/)
- [GitLab](https://gitlab.com/)
- [Bitbucket](https://bitbucket.org/)
- [Git vs GitHub - Atlassian](https://www.atlassian.com/git/tutorials/what-is-git)

## ⏭️ Siguiente Lección

[1.3 - Instalación y Configuración Inicial](03-instalacion-configuracion.md)

---

[⬅️ Lección Anterior](01-introduccion-control-versiones.md) | [🏠 Inicio](../README.md) | [➡️ Siguiente Lección](03-instalacion-configuracion.md)