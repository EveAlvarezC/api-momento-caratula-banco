# Cómo desplegar la app en Streamlit Cloud (gratis)

## Paso 1 — Subir a GitHub

1. Crea una cuenta en https://github.com si no tienes una.
2. Crea un repositorio nuevo (puede ser privado).
3. Sube los 3 archivos de la carpeta `caratulas_app`:
   - `app.py`
   - `requirements.txt`
   - `.streamlit/config.toml`

## Paso 2 — Crear la app en Streamlit Cloud

1. Ve a https://share.streamlit.io y entra con tu cuenta de GitHub.
2. Haz clic en **"New app"**.
3. Selecciona tu repositorio y el archivo `app.py`.
4. En **"Advanced settings"** → **"Secrets"**, pega lo siguiente:

```toml
GEMINI_API_KEY = "tu-api-key-de-gemini-aqui"
```

5. Haz clic en **"Deploy"**. En ~2 minutos tendrás un link público.

## Paso 3 — Compartir

Comparte el link con la persona que va a usar la app.
Solo necesita:
- Abrir el link en su navegador
- Arrastrar los PDFs
- Dar clic en "Procesar"
- Descargar el Excel

No necesita instalar nada.

---

## Para probar en tu computadora (opcional)

```bash
cd caratulas_app
pip install -r requirements.txt
```

Crea el archivo `.streamlit/secrets.toml` con:

```toml
GEMINI_API_KEY = "tu-api-key-aqui"
```

Luego ejecuta:

```bash
streamlit run app.py
```
