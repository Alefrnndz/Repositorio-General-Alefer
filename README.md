# Invitación de cumpleaños — Francisco 🤠

Página única y estática (`index.html`), sin dependencias de build, lista para subir a un subdominio (ej. `francisco.bemarketing.click`).

## Contenido
- Todo vive en `index.html` (HTML + CSS + JS inline). No hay que instalar nada ni compilar nada.
- Fuentes autoalojadas en `assets/fonts/` (no depende de Google Fonts en producción, carga más rápido).
- **Sección hero**: el fondo (`assets/fondo-saya-boys.jpg`) a pantalla completa con el nombre, "¡Cumple 6 años!" y 6 velitas animadas (parpadeo) escritos en vivo sobre la imagen — no es una imagen plana con el texto quemado.
- **Sección de detalles** (al hacer scroll): cuenta regresiva en vivo hasta el sábado 3 de octubre 10:00 (hora La Paz), fecha/hora y dirección en tarjetas, y los botones de acción. Los elementos aparecen con una animación sutil al hacer scroll.
- Botón **"Confirmar por WhatsApp"** abre WhatsApp al número `+591 77284438` con un mensaje pre-escrito.
- Botón **"Cómo llegar"** abre Google Maps con la dirección: *La Casa del Árbol, Calle 20 de Calacoto #7835*.

## Cómo publicarla en `francisco.bemarketing.click`

1. En el panel de hosting de bemarketing (cPanel / Hostinger / cualquiera), crea el subdominio `francisco.bemarketing.click`.
2. Sube `index.html` **y la carpeta `assets/`** (con las 3 imágenes) a la raíz de ese subdominio, vía File Manager o FTP, manteniendo la misma estructura de carpetas.
3. Verifica que el archivo quede exactamente con el nombre `index.html` en la raíz del subdominio.
4. Abre `https://francisco.bemarketing.click` y listo.

No requiere base de datos, PHP, ni ningún backend — es un archivo HTML puro.

## Vista previa al compartir el link (WhatsApp, Facebook, etc.)

El `<head>` de `index.html` incluye etiquetas Open Graph que apuntan a `https://francisco.bemarketing.click/...`. **Si el sitio termina publicado en otro dominio/subdominio**, hay que actualizar esas URLs (busca `og:url`, `og:image` y `twitter:image` en `index.html`) para que coincidan exactamente, o la vista previa no se generará.

WhatsApp cachea la vista previa la primera vez que alguien pega el link. Si haces cambios después de que alguien ya lo compartió, puede seguir mostrando la versión vieja durante un tiempo (agregar `?v=2` al final del link suele forzar una vista previa nueva).

## Personalizar
- Cambiar el número de WhatsApp: buscar `var phone = '59177284438';` dentro de `index.html`.
- Cambiar la dirección del mapa: buscar el `href` del botón "Cómo llegar".
- Cambiar fecha/hora de la cuenta regresiva: buscar `new Date('2026-10-03T10:00:00-04:00')`.
- Cambiar la imagen de vista previa: reemplazar `assets/og-image.jpg` (idealmente 1200×630).
- Cambiar el fondo del hero: reemplazar `assets/fondo-saya-boys.jpg`. Si se agrega una versión vertical optimizada para celular (sin texto, formato retrato), se puede usar en `.hero-bg` con una media query para que no se recorte tanto en pantallas angostas.
