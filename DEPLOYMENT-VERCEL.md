# 🚀 Guía de Deployment en Vercel

## ⚠️ Error 404: NOT_FOUND - SOLUCIÓN

Si ves el error 404, sigue estos pasos:

### 📁 **Estructura de Archivos Correcta:**

```
tu-proyecto/
├── index.html          ← IMPORTANTE: Debe llamarse "index.html"
├── flores-genesis.css
├── vercel.json         ← NUEVO: Archivo de configuración
└── mariposa.webp (opcional)
```

### 🛠️ **Pasos para Subir a Vercel:**

#### **Opción 1: Desde la Terminal (Vercel CLI)**

1. **Instalar Vercel CLI:**
```bash
npm i -g vercel
```

2. **Login:**
```bash
vercel login
```

3. **Deploy:**
```bash
cd tu-proyecto
vercel --prod
```

#### **Opción 2: Desde GitHub (RECOMENDADO)**

1. **Crear repositorio en GitHub**
2. **Subir estos archivos:**
   - `index.html`
   - `flores-genesis.css`
   - `vercel.json`
   - `mariposa.webp` (opcional)

3. **En Vercel.com:**
   - Click "New Project"
   - Importa tu repositorio de GitHub
   - Framework Preset: **Other**
   - Root Directory: `./`
   - Click "Deploy"

#### **Opción 3: Drag & Drop (Más Fácil)**

1. Ve a **vercel.com**
2. Click en "Add New..." → "Project"
3. **Arrastra la carpeta completa** con todos los archivos
4. Click "Deploy"

### ✅ **Checklist de Verificación:**

Antes de hacer deploy, verifica:

- [ ] El archivo se llama `index.html` (no `flores-genesis.html`)
- [ ] Existe el archivo `vercel.json` en la raíz
- [ ] El CSS se llama `flores-genesis.css`
- [ ] La referencia al CSS en index.html es correcta
- [ ] Todos los archivos están en la misma carpeta

### 🔧 **Archivo vercel.json Incluido:**

```json
{
  "rewrites": [
    { "source": "/(.*)", "destination": "/index.html" }
  ]
}
```

### 🚨 **Límites de Vercel (Plan Gratuito):**

- ✅ Despliegues ilimitados
- ✅ Ancho de banda: 100GB/mes
- ✅ Sin límite de commits
- ⚠️ Máximo 100 despliegues por día
- ⚠️ Tiempo de build: 45 min/mes

### 💡 **Si Sigues Viendo 404:**

1. **Limpia el caché de Vercel:**
   - Settings → Deployment → Redeploy

2. **Verifica los logs:**
   - Ve a tu proyecto en Vercel
   - Click en "Deployments"
   - Click en el deployment fallido
   - Revisa "Build Logs"

3. **Verifica las rutas:**
   - Asegúrate que no haya carpetas adicionales
   - Todo debe estar en la raíz

### 📝 **Estructura Correcta para Vercel:**

```
/                         ← Raíz del proyecto
├── index.html           ← Punto de entrada
├── flores-genesis.css   ← Estilos
├── vercel.json          ← Configuración
└── mariposa.webp        ← Recursos
```

### 🔄 **Redeploy Rápido:**

Si ya tienes el proyecto en Vercel:

1. Ve a tu proyecto
2. Settings → Git
3. Click "Redeploy" en el último commit
4. O haz un nuevo commit/push

### ⚡ **Solución Rápida al 404:**

El problema más común es que el archivo no se llama `index.html`.

**Solución:**
```bash
# Renombra el archivo
mv flores-genesis.html index.html

# O crea una copia
cp flores-genesis.html index.html
```

### 🎯 **URL Final:**

Después del deploy exitoso, tu jardín estará en:
```
https://tu-proyecto.vercel.app
```

---

## 📦 **Archivos Incluidos en Este Package:**

1. **index.html** - Jardín mágico principal
2. **flores-genesis.css** - Estilos con colores suaves
3. **vercel.json** - Configuración de Vercel
4. **mariposa.webp** - Imagen de mariposa (opcional)

---

**¡Todo listo para deployment exitoso!** 🚀✨

Si el problema persiste, comparte el enlace de tu repositorio o proyecto de Vercel para ayudarte mejor.
