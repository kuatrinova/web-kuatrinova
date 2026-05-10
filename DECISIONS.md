# Decisiones técnicas — Landing Page Kuatrinova

No reabrir una decisión sin motivo técnico sólido.

## ADR-001 — Stack vanilla (HTML/CSS/JS) sin frameworks
- **Decisión:** Mantener el sitio en HTML5 + CSS3 + JavaScript vanilla, sin frameworks (React, Vue, Next, etc.) ni build step.
- **Motivo:** Es una landing de marketing simple. Vanilla minimiza tiempo de carga, simplifica el deploy en Hostinger compartido y elimina dependencias de mantenimiento.
- **Estado:** ✅ Firme

## ADR-002 — Hosting en Hostinger
- **Decisión:** Servir el sitio desde Hostinger con configuración vía `.htaccess`.
- **Motivo:** Hosting ya contratado, suficiente para un sitio estático, soporte de Apache permite redirects y headers sin servidor propio.
- **Estado:** ✅ Firme

## ADR-003 — No migrar a WordPress (de momento)
- **Decisión:** Mantener el stack vanilla y no abrir blog ni migrar a WordPress hasta que exista una automatización (n8n + IA) que genere contenido de forma sostenible.
- **Motivo:** Un blog manual no es sostenible para el ritmo del proyecto y un blog vacío perjudica el SEO en lugar de ayudarlo. La premisa "WordPress = mejor SEO" es falsa: el HTML estático actual posiciona igual o mejor en Core Web Vitals. La migración solo se justifica cuando haya pipeline de contenido automatizado.
- **Estado:** ✅ Firme — revisar cuando exista la automatización de generación de posts.

---

_Añadir nuevas entradas aquí cuando se tome una decisión relevante._
