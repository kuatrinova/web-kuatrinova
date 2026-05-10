# Convenciones — Landing Page Kuatrinova

## Código
- Comentarios en español
- Clases: PascalCase
- Métodos y variables: camelCase
- Constantes: UPPER_SNAKE_CASE
- async/await con try/catch siempre

## HTML / CSS
- HTML5 semántico (`<header>`, `<main>`, `<section>`, `<footer>`)
- Clases CSS en kebab-case (`.hero-section`, `.btn-primary`)
- Mobile-first: media queries con `min-width`
- Imágenes en `/assets`, optimizadas (WebP/JPG comprimido)

## SEO
- Cada página HTML debe tener: `<title>`, `<meta name="description">`, Open Graph tags
- Mantener `sitemap.xml` y `robots.txt` actualizados al añadir páginas

## Base de datos
No aplica (sitio estático).

## API
No aplica (sitio estático). Contacto vía `mailto:info@kuatrinova.es` con `subject` específico por servicio/página. Si en el futuro se añade un endpoint/formulario:
- REST estándar
- Respuesta siempre: `{ "success": bool, "data": {}, "message": "" }`

## Git
- Commits en español, imperativo: "Añadir validación en formulario"
- No commitear `.env` ni credenciales
- Rama principal: `main`

## Lo que NO hacer
- No cambiar convenciones sin registrar en DECISIONS.md
- No añadir librerías sin consultar (mantener stack vanilla)
- No introducir frameworks (React, Vue, etc.) sin decisión explícita
