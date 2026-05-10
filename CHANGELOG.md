# Changelog — Landing Page Kuatrinova

El agente actualiza este archivo al finalizar cada sesión de trabajo.
Entradas más recientes arriba.

## 2026-05-10
- Creada estructura de documentación del proyecto (CLAUDE.md, ARCHITECTURE.md, CONVENTIONS.md, DECISIONS.md, CHANGELOG.md, memory/progress.md, memory/context.md)
- Audit SEO inicial — hallazgos pendientes en su momento
- ADR-003: no migrar a WordPress hasta tener automatización de contenido
- **Tracking GA4 + GTM completo:**
  - GA4 property "Kuatrinova" (id 536940191, measurement_id G-PXKCC10MD7) en cuenta 388745006
  - GTM cuenta 6354443797 + contenedor GTM-TMTDNCJ3 con tag GA4 + trigger All Pages publicado
  - Snippet GTM en las 8 páginas HTML
  - Verificado en GA4 → Tiempo real
- **Incidente de deploy resuelto:** el "Implementar" del panel Git de Hostinger clona en `public_html/public_html/` (subdir) en lugar del raíz. Workaround documentado: SSH + `git reset --hard origin/main` desde `~/domains/kuatrinova.es/public_html/`.
- **Mejoras SEO técnicas (commit f0a777d):**
  - sitemap.xml con 8 URLs (era solo la home)
  - .htaccess: redirect 301 www→non-www
  - Schema JSON-LD en las 8 páginas (ProfessionalService + WebSite en index, Service + BreadcrumbList en internas)
  - Open Graph + Twitter Cards completos en internas (faltaban og:url, og:type, twitter:*)
  - Tildes corregidas en titles y meta descriptions
- **Search Console verificada** (auto-verificación por proveedor de dominio) y sitemap enviado
- **Windsor.ai conectado:** GA4 Kuatrinova (536940191) y GSC kuatrinova.es añadidos al hub central de GROWTH_AGENT
