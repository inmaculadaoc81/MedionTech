MedionTech ONE PAGE

Dominio:
https://informaticoschamberi.com.es/

(Antes tenía https://123pcsolutions.com.es/, dominio duplicado con
ToshibaTech de la misma familia. Confirmado por el cliente: el dominio
real de MedionTech es informaticoschamberi.com.es. Aplicado en
canonical, og:url, JSON-LD, robots.txt y sitemap.xml. ToshibaTech
mantiene 123pcsolutions.com.es.)

Teléfono SOLO en caja de información:
+34 910 05 36 51

Teléfono en todos los botones telefónicos:
+34 914 46 85 03

Incluye:
- WhatsApp 24/365
- Recogida
- Atención telefónica
- Google Business
- YouTube
- Cal.com
- Formulario SMTP
- Chatbot n8n
- Mapa
- SEO One Page
- Sección específica Medion: pantalla, batería, placa base, SSD, teclado/touchpad y refrigeración

IMPORTANTE:
No se proporcionó información sobre coste o gratuidad del diagnóstico para esta web, por lo que no se ha inventado ni mostrado ningún precio de diagnóstico.

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo de soporte no aparece visible en el HTML; solo se utiliza en /api/contacto.

Google Analytics:
G-Y5W07S9DP3

REVISIÓN (fixes adicionales aplicados):
- Ya tenía menú móvil, colisión del chatbot corregida, schema.org y
  sección SEO (de commits anteriores); no se ha tocado nada de eso.
- Añadido borde blanco (border:1px solid #fff!important) al botón del
  chat, que faltaba tanto en CSS como en el script JS de
  reposicionamiento.
- Botón de teléfono del menú (.navcall): acortado a solo el número
  (mismo problema de línea partida visto en otros repos de la familia);
  añadido white-space:nowrap.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar / Política
  de privacidad → https://kelatos.com/privacy-policy/), con diseño
  apilado a ancho completo en móvil.

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home.
Añadida la dependencia "@vercel/functions" en package.json.

REVISIÓN ADICIONAL (a petición del cliente):
1. H1 no seguía la regla final de la familia: era largo (23 palabras)
   y terminaba en planteamiento abierto ("y cuándo podrás volver a
   usarlo"). Reescrito: "Tu Medion no funciona. Aquí lo revisamos y lo
   reparamos." (9 palabras, afirmativo).
2. La tarjeta azul de la sección "Sobre Medion" (.hardware-art) tenía
   como marca de agua decorativa el texto "HARDWARE", que en móvil se
   veía enorme y cortado (solo se leía "HARD"). Sustituido por
   "MEDION" (el nombre del producto, como pediste) y añadida una
   reducción de tamaño específica en los breakpoints de tablet (60px)
   y móvil (48px), que antes no existía — antes el texto se quedaba
   siempre a 82px sin importar el ancho de pantalla.
3. Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
   del horario en la caja de información.
4. Añadida una franja de aviso ("Somos un servicio técnico
   independiente. No vemos equipos en garantía.") justo debajo de la
   barra de menú, antes del hero.
5. Formulario de contacto verificado: el fetch de index.html apunta a
   /api/contacto, los nombres de campo (nombre/telefono/email/equipo/
   mensaje) coinciden exactamente entre el HTML y lo que valida
   api/contacto.js, la API usa SMTP + nodemailer correctamente y
   package.json/vercel.json están bien configurados. Conexión
   correcta de principio a fin (solo falta que las variables SMTP_*
   estén configuradas en Vercel, como en el resto de la familia). De
   paso se corrigió un resto del dominio antiguo: el asunto del correo
   decía "...123pcsolutions.com.es" (el dominio de antes de la
   corrección aplicada hoy); actualizado a
   "...informaticoschamberi.com.es".

REVISIÓN ADICIONAL 2 (a petición del cliente):
6. La casilla del formulario "Acepto la política de privacidad" no
   tenía ningún enlace. Añadido, apuntando a
   https://kelatos.com/privacy-policy/ (mismo texto/enlace exigido
   ahora como estándar para toda la familia — aplicar en el resto de
   repos que se procesen a partir de ahora).
7. El botón "Atención Telefónica 24 horas 365 días" no tenía icono, a
   diferencia del botón de WhatsApp de al lado. Añadido el icono de
   teléfono (mismo SVG usado en otros repos de la familia), usando la
   regla .cta svg ya existente.
