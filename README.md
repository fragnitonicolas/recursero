# Recursero Departamental — Comisión de Familia CMFJAL

Buscador de recursos sociales con interfaz de chatbot para Avellaneda y Lanús.  
Usa la API gratuita de Google Gemini para interpretar consultas en lenguaje natural y devolver los recursos más relevantes del dataset.

---

## 1. Obtener la API Key de Google Gemini (gratis)

1. Ir a [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Iniciar sesión con una cuenta de Google
3. Hacer clic en **"Create API key"**
4. Copiar la clave generada

---

## 2. Configurar la API Key localmente

Crear (o editar) el archivo `config.js` en la raíz del proyecto:

```js
const GEMINI_API_KEY = "PEGAR_ACA_LA_CLAVE";
```

> **Importante:** `config.js` está en `.gitignore` y **nunca se sube al repositorio**.  
> Nunca compartas ni publiques tu API key.

---

## 3. Configurar la API Key en GitHub Pages

Para que la app funcione en producción (GitHub Pages), la API key debe incluirse en el deploy.  
La forma más segura y simple:

1. En el repositorio de GitHub, ir a **Settings → Secrets and variables → Actions**
2. Crear un secret llamado `GEMINI_API_KEY` con el valor de tu clave
3. El workflow de deploy (`.github/workflows/deploy.yml`) inyecta la clave automáticamente al hacer push

---

## 4. Deploy en GitHub Pages

El repositorio ya tiene GitHub Pages habilitado sobre la rama `main`.  
Cada push a `main` actualiza la app automáticamente.

```bash
git add index.html
git commit -m "actualización"
git push
```

La URL pública es: `https://<tu-usuario>.github.io/recursero/`

---

## Aviso

Esta herramienta es **orientativa**. No reemplaza la intervención profesional ni la atención de urgencias.  
**Ante una emergencia, llamar al 911.**
