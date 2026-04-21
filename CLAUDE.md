# Iglesia Multimedia — Landing Page

## Qué es esto
Landing page de captura de leads para el newsletter/curso de IA para iglesias y ministerios hispanohablantes. El objetivo es que pastores, líderes y equipos de comunicación se suscriban y reciban la guía gratuita "5 Herramientas de IA para tu iglesia".

## Estructura
- Proyecto de un solo archivo: `index.html` (HTML + CSS + JS inline, sin build, sin dependencias NPM)
- Sin framework. Vanilla JS puro.
- Desplegable directamente en cualquier hosting estático (Netlify, Vercel, GitHub Pages)

## Secciones de la página
1. **Navbar** — fijo, se vuelve blanco al hacer scroll
2. **Hero** — titular + CTA + mockup del PDF lead magnet
3. **Proof bar** — beneficios rápidos (gratuito, sin spam, para cualquier iglesia)
4. **Benefits** — 4 tarjetas con lo que el suscriptor recibe cada viernes
5. **Lead magnet** — lista de las 5 herramientas de la guía
6. **Formulario** — nombre + email → abre Substack con email precargado
7. **About** — bio de Alejo Caicedo
8. **Footer**

## Paleta de colores
```
--navy:  #0D1B2A  (fondo oscuro principal)
--blue:  #1A6FD4  (azul acento)
--teal:  #00D4AA  (teal principal, CTAs y checks)
--ink:   #0A1628  (texto oscuro)
--paper: #FFFFFF
--gray:  #F7F8FA  (fondos claros)
--muted: #5a6577  (texto secundario)
```

## Tipografías
- **Space Grotesk** (500/600/700) — headings y logo
- **Plus Jakarta Sans** (400/500/600/700) — cuerpo de texto
- Ambas se cargan desde Google Fonts

## Formulario / Lead capture
- El form captura nombre y email
- Al enviar abre `https://alejocaicedo.substack.com/subscribe?email=<email>` en nueva pestaña
- No hay backend propio; Substack gestiona la suscripción
- Tras enviar: oculta el form y muestra el mensaje de éxito `.form-success`

## Autor y marca
- **Alejo Caicedo** — responsable de multimedia en iglesia evangélica en Córdoba, España
- Marca digital: **Pulpo Digital** (marketing, IA, automatización)
- Newsletter: `alejocaicedo.substack.com`
- YouTube: `youtube.com/@alejocaicedo`
- Email: `alejo@pulpodigital.es`

## Convenciones de código
- Todo el CSS está en `<style>` dentro del `<head>` — mantener este patrón
- Todo el JS está en `<script>` al final del `<body>`
- Clases BEM-like pero simplificadas (`.card`, `.card-icon`, `.card h3`)
- Animaciones de entrada: clase `.reveal` + IntersectionObserver que añade `.in`
- Responsive breakpoint principal: `@media (max-width: 860px)`

## Lo que NO hacer
- No añadir frameworks (React, Vue, etc.)
- No separar en múltiples archivos sin necesidad real
- No cambiar la paleta de colores sin validar con el usuario
- No modificar el flujo del formulario (Substack) sin confirmar
