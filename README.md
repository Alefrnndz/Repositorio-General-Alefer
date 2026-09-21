# Invitación de cumpleaños — Francisco 🤠

Página única y estática (`index.html`), sin dependencias de build, lista para subir a un subdominio (ej. `francisco.bemarketing.click`).

## Contenido
- Todo vive en `index.html` (HTML + CSS + JS inline). No hay que instalar nada ni compilar nada.
- Fuentes desde Google Fonts (CDN), el resto es autocontenido.
- Botón **"Confirmar por WhatsApp"** abre WhatsApp al número `+591 77284438` con un mensaje pre-escrito.
- Botón **"Cómo llegar"** abre Google Maps con la dirección: *La Casa del Árbol, Calle 20 de Calacoto #7835*.
- Cuenta regresiva en vivo hasta el sábado 3 de octubre, 10:00 (hora La Paz).

## Cómo publicarla en `francisco.bemarketing.click`

1. En el panel de hosting de bemarketing (cPanel / Hostinger / cualquiera), crea el subdominio `francisco.bemarketing.click`.
2. Sube el archivo `index.html` a la carpeta raíz de ese subdominio (por ejemplo `public_html/francisco/` o la que el panel asigne automáticamente), vía File Manager o FTP.
3. Verifica que el archivo quede exactamente con el nombre `index.html` en la raíz del subdominio.
4. Abre `https://francisco.bemarketing.click` y listo.

No requiere base de datos, PHP, ni ningún backend — es un archivo HTML puro.

## Personalizar
- Cambiar el número de WhatsApp: buscar `var phone = '59177284438';` dentro de `index.html`.
- Cambiar la dirección del mapa: buscar el `href` del botón "Cómo llegar".
- Cambiar fecha/hora de la cuenta regresiva: buscar `new Date('2026-10-03T10:00:00-04:00')`.
