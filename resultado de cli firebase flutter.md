Vas a necesitar algo más que copiar comandos: si no dejas bien instalado **Node + npm + Firebase CLI**, Flutter no va a conectar nunca con Firebase. Te lo explico claro y paso a paso para Windows 👇

---

# 🧰 1. Software necesario

Para trabajar con Firebase CLI necesitas:

* Node.js
* npm (se instala junto con Node)
* Firebase CLI

---

# 🔍 2. Verificar si ya tienes Node y npm

Abre **CMD o PowerShell** y escribe:

```bash
node -v
npm -v
```

✔ Si ves algo como:

```
v20.10.0
9.8.1
```

→ Ya lo tienes instalado

❌ Si dice *“no se reconoce el comando”* → NO está instalado

---

# 📥 3. Instalar Node.js (incluye npm)

1. Ve a:
   👉 Node.js

2. Descarga la versión **LTS (recomendada)**

3. Ejecuta el instalador:

   * Siguiente → Siguiente
   * ✔ Marca “Add to PATH”
   * Instalar

4. Reinicia tu computadora (importante)

---

# 🔁 4. Verificar instalación otra vez

```bash
node -v
npm -v
```

Si ahora sí aparecen versiones → listo ✅

---

# 🌍 5. Instalar Firebase CLI (global)

Aquí es donde muchos fallan. Debe ser **global**:

```bash
npm install -g firebase-tools
```

✔ `-g` = instalación global (desde cualquier proyecto)

---

# 🔍 6. Verificar Firebase CLI

```bash
firebase --version
```

Si ves un número → todo bien
Si no → reinicia terminal

---

# 🔐 7. Iniciar sesión en Firebase (Google)

Este paso conecta tu PC con tu cuenta:

```bash
firebase login
```

👉 Se abrirá el navegador
👉 Inicia sesión con tu cuenta de Google
👉 Acepta permisos

✔ Regresas a la terminal con:

```
✔ Success! Logged in as tucorreo@gmail.com
```

---

# 🚪 8. Comandos básicos de Firebase CLI

## 🔹 Ver proyectos

```bash
firebase projects:list
```

---

## 🔹 Inicializar Firebase en tu proyecto Flutter

(IMPORTANTE: dentro de tu carpeta del proyecto)

```bash
firebase init
```

Selecciona:

* Firestore
* Hosting (opcional)

---

## 🔹 Conectar Flutter con Firebase (recomendado)

Usa:

```bash
dart pub global activate flutterfire_cli
flutterfire configure
```

Esto genera automáticamente:

```
firebase_options.dart
```

---

# ⚠️ ERRORES comunes (te ahorro tiempo)

❌ “firebase no se reconoce”
→ No instalaste global o falta reiniciar terminal

❌ “npm no reconocido”
→ Node no está en PATH

❌ No abre login
→ Usa:

```bash
firebase login --no-localhost
```

---

# 🧠 Resumen rápido (lo que debes hacer)

1. Instalar Node.js
2. Verificar `node -v` y `npm -v`
3. Instalar Firebase CLI:

   ```bash
   npm install -g firebase-tools
   ```
4. Login:

   ```bash
   firebase login
   ```
5. Configurar proyecto:

   ```bash
   firebase init
   ```

---

Si quieres, en el siguiente paso te enseño:
👉 cómo conectar TODO esto con tu CRUD de usuarios en Flutter
👉 o cómo usar Antigravity directamente con Firebase

Solo dime 👍
