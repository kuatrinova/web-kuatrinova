# Estado actual del proyecto

**Última actualización:** 2026-05-10
**Actualizado por:** agente

## Estado general
🟢 En producción con tracking GA4/GTM funcionando

## Tracking + SEO técnico (live desde 10/05/2026)
- GA4 Property `536940191` ("Kuatrinova" en cuenta 388745006), Measurement ID `G-PXKCC10MD7`
- GTM Container `GTM-TMTDNCJ3` (cuenta `6354443797`) con tag GA4 + trigger All Pages
- Snippet GTM en las 8 HTMLs (head + body noscript) — verificado en GA4 Tiempo real
- Search Console verificada (auto vía proveedor de dominio) + sitemap.xml enviado
- Schema JSON-LD: ProfessionalService + WebSite en index; Service + BreadcrumbList en las 7 internas
- Open Graph + Twitter Cards completos en las 8 páginas
- Redirect 301 www→non-www en .htaccess
- Sitemap.xml con las 8 URLs
- Windsor.ai (hub central): GA4 Kuatrinova (536940191) + GSC kuatrinova.es conectados

## Pendiente (próxima sesión)
1. **Tildes en body de páginas internas**: ~30 cambios (Automatizacion→Automatización, gestion→gestión, etc.) Carlos prefirió saltarlo en esta sesión por bajo impacto SEO real.
2. **Cross-linking entre servicios**: cada servicio solo enlaza al index. Sería un boost SEO añadir 2-3 links contextuales entre servicios relacionados (automatización↔integraciones↔chatbots).
3. **Pixel de Meta**: pendiente decisión cuando se planifiquen ads en Instagram/Facebook.
4. **og-image específica por servicio**: ahora todas comparten `og-image.jpg`. Una por servicio mejora CTR en redes.
5. **Optimización de imágenes a WebP** (logos en PNG, og-image en JPG).

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
