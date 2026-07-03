# Dashboard Financiero - Condominio El Amanecer

Plataforma de visualización de datos financieros y de infraestructura diseñada para la administración transparente de recursos comunitarios.

## Arquitectura del Sistema
Este proyecto utiliza una arquitectura **Serverless y Edge Computing**:
* **Frontend:** HTML5 semántico, Tailwind CSS (vía CDN) y Chart.js.
* **Backend / Base de Datos:** Google Sheets interactuando como una base de datos en tiempo real mediante la **Google Visualization API**.
* **Hosting:** GitHub Pages (Despliegue estático, alta disponibilidad).

## Requisitos Previos (Google Sheets)
El sistema extrae datos del Google Sheets con ID: `1lcySRnqq8ViScL9iVtvpPbSU-Pp1RHLEUxwfM23O5uo`.
Para que el puente de datos funcione, el documento debe estar configurado de la siguiente manera:
1. En Google Sheets, clic en **Compartir**.
2. Cambiar "Acceso general" a **"Cualquier persona con el enlace"**.
3. Rol establecido como **"Lector"**.

### Estructura de Pestañas
El script busca las siguientes hojas exactamente por nombre:
* `adherencia`
* `socios al dia`
* `cajaConreparaciones`
* `Reparaciones`

## Guía de Despliegue en GitHub Pages
1. Crea un nuevo repositorio público en tu cuenta de GitHub.
2. Sube los archivos `index.html` y `README.md` a la rama `main`.
3. Ve a la pestaña **Settings** (Configuración) del repositorio.
4. En la barra lateral izquierda, selecciona **Pages**.
5. Bajo "Build and deployment", selecciona como fuente (Source) la rama `main` y la carpeta `/ (root)`.
6. Haz clic en **Save**. 
7. En unos minutos, GitHub te proporcionará una URL pública (ej. `https://tu-usuario.github.io/tu-repo/`) donde el dashboard estará online y actualizándose en tiempo real conforme edites tu Google Sheet.