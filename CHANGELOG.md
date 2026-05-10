# Changelog — Landing Page Kuatrinova

El agente actualiza este archivo al finalizar cada sesión de trabajo.
Entradas más recientes arriba.

## 2026-05-10
- Creada estructura de documentación del proyecto (CLAUDE.md, ARCHITECTURE.md, CONVENTIONS.md, DECISIONS.md, CHANGELOG.md, memory/progress.md, memory/context.md)
- Audit SEO inicial — hallazgos pendientes: sitemap incompleto, sin schema, sin redirect www, tildes en titles
- ADR-003: no migrar a WordPress hasta tener automatización de contenido
- Configurado tracking completo:
  - GA4 property "Kuatrinova" creada (id 536940191, measurement_id G-PXKCC10MD7) en cuenta 388745006
  - GTM cuenta 6354443797 + contenedor GTM-TMTDNCJ3 con tag GA4 + trigger All Pages publicado
  - Snippet GTM insertado en las 8 páginas HTML
- Deploy a Hostinger via SSH (manual): el "Implementar" del panel Git de Hostinger clonó en `public_html/public_html/` (subdir) en lugar del raíz; corregido moviendo archivos al directorio correcto vía SSH
- Tracking verificado funcionando en GA4 → Tiempo real
