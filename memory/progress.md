# Estado actual del proyecto

**Última actualización:** 2026-05-10
**Actualizado por:** agente

## Estado general
🟢 En producción con tracking GA4/GTM funcionando

## Tracking configurado (live desde 10/05/2026)
- GA4 Property: id `536940191` ("Kuatrinova" en cuenta 388745006)
- Measurement ID: `G-PXKCC10MD7`
- GTM: Account `6354443797`, Container `GTM-TMTDNCJ3` con tag GA4 + trigger All Pages
- Snippet en las 8 HTMLs (head + body noscript)
- Verificado funcionando en GA4 Tiempo real

## Pendiente (próxima sesión)
1. **Deploy futuro**: el "Implementar" del panel Git de Hostinger clona en `public_html/public_html/` (subdir) en lugar de directamente en raíz. Workaround actual: tras cada `git push`, conectar por SSH y mover archivos. Pendiente decidir flujo definitivo (SSH script automatizado / borrar y reconfigurar Git deploy / webhook).
2. **Conectar a Windsor.ai**: añadir nueva propiedad GA4 (536940191) + Search Console (kuatrinova.es) al MCP de GROWTH_AGENT para que aparezcan en el dashboard centralizado.
3. **Verificar dominio en Search Console** vía DNS TXT (panel Hostinger DNS).
4. **Resto de hallazgos del audit SEO inicial:**
   - sitemap.xml solo lista la home → añadir las 7 páginas de servicios
   - Schema markup JSON-LD (Organization en index, Service + BreadcrumbList en internas)
   - Redirect www → non-www en .htaccess
   - Tildes y caracteres en titles/descriptions ("Automatizacion" → "Automatización", etc.)
   - OG tags incompletos en páginas internas (les falta og:url, og:type, twitter cards)
   - Cross-linking entre servicios (cada servicio solo enlaza al index, sin links a servicios relacionados)
5. **Pixel de Meta**: pendiente decisión (Carlos respondió "lo decidimos más adelante"). Cuando se decida hacer ads de Instagram/Facebook, instalar.

## Bloqueantes
- Ninguno

## Notas última sesión
**2026-05-10** — Sesión larga (~3h):
1. Reestructuración de documentación del proyecto (CLAUDE.md actualizado + ARCHITECTURE/CONVENTIONS/DECISIONS/CHANGELOG/memory creados)
2. Audit SEO inicial (hallazgos en TODOs)
3. Decisión ADR-003: no migrar a WordPress hasta tener automatización de contenido
4. Configuración completa de tracking GA4 + GTM (vía API y SSH al hosting)
5. Resolución de incidente de deploy: Hostinger Git deploy clonó en subdirectorio incorrecto, fix manual vía SSH
6. Verificación final: tracking visible en GA4 Tiempo real ✅
