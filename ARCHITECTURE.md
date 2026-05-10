# Arquitectura — Landing Page Kuatrinova

## Stack
| Capa | Tecnología |
|------|-----------|
| Backend | No aplica (sitio estático) |
| Base de datos | No aplica |
| Frontend | HTML5 + CSS3 + JavaScript vanilla |
| Servidor | Hostinger (hosting compartido + .htaccess) |

## Módulos principales
- **index.html** — landing principal
- **auditoria.html** — página de servicio: auditoría
- **automatizacion.html** — página de servicio: automatización
- **chatbots.html** — página de servicio: chatbots
- **dashboards.html** — página de servicio: dashboards
- **diseno.html** — página de servicio: diseño
- **implementacion.html** — página de servicio: implementación
- **integraciones.html** — página de servicio: integraciones
- **style.css** — hoja de estilos global
- **script.js** — JS de interacción global

## Flujo de datos
Sitio puramente estático. No hay backend ni API. El usuario navega entre páginas HTML servidas directamente por Hostinger. No se almacenan datos del visitante en cliente ni servidor (más allá de logs estándar del hosting).

## Estructura de carpetas
```
/                  → páginas HTML (raíz plana)
/assets            → imágenes y recursos estáticos
/.htaccess         → configuración de Apache (redirects, headers)
/sitemap.xml       → sitemap SEO
/robots.txt        → directrices de crawlers
/style.css         → estilos
/script.js         → JS
```

## Integraciones externas
- **Hosting:** Hostinger
- **Dominio:** https://kuatrinova.es
- **Analytics / píxeles:** Ninguno actualmente (no hay GA, GTM, Facebook Pixel, Hotjar ni Clarity en ningún HTML)
- **Formularios de contacto:** No hay formularios HTML. Todos los CTAs de contacto usan `mailto:info@kuatrinova.es` con `subject` preformateado por página/servicio
