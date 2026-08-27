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
