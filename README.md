# 🚀 Bienvenidos al curso

¡Bienvenidos! 👋

Este espacio de GitHub será el punto de encuentro para trabajar durante el curso. Aquí encontrarás los proyectos, prácticas y actividades que iremos desarrollando a lo largo del semestre.

La idea es que, además de aprender los contenidos del curso, puedas adquirir experiencia trabajando con **Git y GitHub**, herramientas utilizadas habitualmente para desarrollar y mantener proyectos de software.

---

## 🎯 ¿Cómo trabajaremos?

Cada estudiante deberá tener **su propio repositorio de GitHub para el proyecto**.

📦 Tu repositorio será el lugar donde guardarás:

* 💻 Código fuente
* 📝 Documentación
* 📈 Avances del proyecto
* 🔄 Diferentes versiones de tu trabajo
* 🎤 Material necesario para la presentación final

> [!TIP]
> No esperes hasta el último momento para subir tu proyecto.
> Haz commits frecuentemente. Git está pensado para guardar la historia de tu trabajo.

---

# 📊 ¿Cómo se evaluará?

### 🚫 No habrá examen

La evaluación se realizará mediante el trabajo desarrollado durante el curso.

| Concepto                                     | Porcentaje |
| -------------------------------------------- | :--------: |
| 📝 Prácticas y actividades de clase          |   **30%**  |
| 🚧 Avances del proyecto / proyecto terminado |   **40%**  |
| 🎤 Presentación del proyecto                 |   **20%**  |
| 👥 Asistencia                                |   **10%**  |
| **Total**                                    |  **100%**  |

### 📌 Importante sobre la asistencia

La asistencia representa **10% de la calificación final**.

Además, deberás cumplir con **al menos el 90% de asistencia en cada parcial**.

> [!WARNING]
> Si tu asistencia durante un parcial es menor al 90%, se aplicará una **penalización sobre la calificación final**.
> 4 Retardos acumulados cuentan como una falta, un retardo se considera después de 🕗8:10

> [!TIP]
> 👀 La asistencia no solamente significa estar presente: también es importante participar y trabajar durante las sesiones.

---

# 🧑‍💻 Git y GitHub

No necesitas ser experto en Git para comenzar.

Piensa en Git como una **máquina del tiempo para tu proyecto** ⏳:

```text
💻 Trabajas
   ↓
📦 Guardas cambios
   ↓
📸 Commit
   ↓
☁️ GitHub
   ↓
🔄 Puedes recuperar tu proyecto
```

A continuación encontrarás los comandos que más utilizarás.

---

# 🟢 1. Preparar Git

Antes de comenzar, puedes comprobar que Git está instalado:

```bash
git --version
```

Configura tu nombre:

```bash
git config --global user.name "Tu Nombre"
```

Configura tu correo:

```bash
git config --global user.email "tu-correo@example.com"
```

---

# 📸 2. Guardar cambios con un Commit

Un **commit** es como tomar una fotografía de tu proyecto en un momento determinado.

### Paso 1 — Revisar qué cambió

```bash
git status
```

Esto te permite saber qué archivos fueron modificados, agregados o eliminados.

```text
📁 archivo-modificado
📄 archivo-nuevo
❌ archivo-eliminado
```

---

### Paso 2 — Agregar archivos

Para agregar un archivo específico:

```bash
git add archivo.cpp
```

Para agregar todos los cambios:

```bash
git add .
```

---

### Paso 3 — Revisar qué se va a guardar

```bash
git status
```

> [!NOTE]
> Este paso es recomendable antes de hacer el commit.

---

### Paso 4 — Quitar un archivo del próximo commit

¿Agregaste algo por accidente?

```bash
git restore --staged archivo.cpp
```

> [!NOTE]
> El archivo **no se elimina**. Simplemente deja de estar preparado para el commit.

---

### Paso 5 — Crear el commit

```bash
git commit -m "Agrega implementación de lista enlazada"
```

Un buen mensaje debe explicar **qué cambiaste**.

✅ Mejor:

```bash
git commit -m "Agrega función para insertar nodos"
```

❌ Evita:

```bash
git commit -m "cosas"
```

```bash
git commit -m "cambios"
```

---

# ☁️ 3. Conectar tu proyecto con GitHub

Si ya tienes un repositorio creado en GitHub y tienes un proyecto local:

```bash
git init
```

Agrega el repositorio remoto:

```bash
git remote add origin https://github.com/USUARIO/REPOSITORIO.git
```

Puedes comprobar que quedó conectado:

```bash
git remote -v
```

---

# 📥 4. Obtener cambios desde GitHub

Si el repositorio ya existe y quieres descargar sus cambios:

```bash
git pull
```

También puedes especificar:

```bash
git pull origin main
```

📥 **Pull = traer cambios desde GitHub hacia tu computadora.**

```text
☁️ GitHub
   ↓
 git pull
   ↓
💻 Tu computadora
```

---

# 📤 5. Subir tus cambios a GitHub

Después de hacer tu commit:

```bash
git push
```

O indicando el repositorio y la rama:

```bash
git push origin main
```

📤 **Push = enviar tus commits a GitHub.**

```text
💻 Tu computadora
   ↓
 git push
   ↓
☁️ GitHub
```

---

# 🔄 6. El ciclo que utilizarás normalmente

En el día a día probablemente utilizarás principalmente estos comandos:

```bash
git status

git add .

git status

git commit -m "Describe tu cambio"

git push
```

Y cuando necesites obtener cambios:

```bash
git pull
```

### 🧠 En resumen

```text
👀 ¿Qué cambió?
git status

➕ Preparar cambios
git add .

📸 Guardar una versión
git commit -m "mensaje"

☁️ Subir a GitHub
git push

📥 Descargar cambios
git pull
```

---

# 🧭 7. Comandos útiles

### 📜 Ver el historial

```bash
git log
```

Una versión más sencilla de leer:

```bash
git log --oneline
```

Ejemplo:

```text
a31f52a Agrega búsqueda de estudiantes
92bd821 Corrige eliminación de nodos
7ac123f Crea estructura inicial
```

---

### 🌿 Ver las ramas

```bash
git branch
```

Crear una nueva rama:

```bash
git branch nombre-rama
```

Cambiar de rama:

```bash
git switch nombre-rama
```

Crear y cambiar a una nueva rama:

```bash
git switch -c nombre-rama
```

> [!TIP]
> 🌱 Las ramas permiten trabajar en cambios sin modificar directamente la versión principal del proyecto.

---

### 🔍 Comparar cambios

```bash
git diff
```

Te permite revisar qué modificaste antes de hacer el commit.

---

# 🆘 ¿Te equivocaste?

No entres en pánico. 😅

Git permite recuperar muchas situaciones.

Si agregaste un archivo al staging por error:

```bash
git restore --staged archivo.cpp
```

Si modificaste un archivo pero quieres descartar esos cambios:

```bash
git restore archivo.cpp
```

> [!CAUTION]
> Este último comando elimina los cambios locales que todavía no hayas guardado en un commit.

---

# ⭐ Recomendaciones para el proyecto

### 1️⃣ Haz commits pequeños

No esperes a terminar todo el proyecto.

```text
❌ Un commit después de 3 semanas

✅ Muchos commits pequeños durante el desarrollo
```

### 2️⃣ Escribe mensajes claros

```bash
git commit -m "Agrega menú principal"
git commit -m "Implementa búsqueda"
git commit -m "Corrige eliminación de elementos"
```

### 3️⃣ Sube frecuentemente tu trabajo

```bash
git push
```

Tu repositorio también funciona como respaldo. ☁️

### 4️⃣ Revisa antes de hacer commit

```bash
git status
git diff
```

### 5️⃣ No subas archivos innecesarios

Por ejemplo:

```text
❌ archivos temporales
❌ archivos generados automáticamente
❌ contraseñas
❌ claves privadas
❌ carpetas innecesarias del IDE
```

💡 Para esto utilizaremos `.gitignore`.

---

# 🚀 Tu proyecto empieza aquí

Tu repositorio será más que una carpeta con código.

Será la **historia de cómo construiste tu proyecto**:

```text
💡 Idea
  ↓
📝 Primer código
  ↓
🔨 Desarrollo
  ↓
🐛 Correcciones
  ↓
✨ Mejoras
  ↓
🚀 Proyecto terminado
  ↓
🎤 Presentación
```

No busques hacer todo perfecto desde el principio.

**Construye → guarda → mejora → vuelve a guardar.**

¡Manos a la obra! 👨‍💻👩‍💻

---

# ℹ️ Recursos

Si aún tienes dudas sobre Git pero quieres practicar, puedes utilizar la siguiente web para practicar los comando sin necesidad de eliminar o arruinar algo de tu proyecto.
https://learngitbranching.js.org/?locale=es_MX
