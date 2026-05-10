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
- Tildes correctas en titles, descriptions y body de las 7 internas (~50 cambios)
- Cross-linking temático ("Servicios relacionados") antes del CTA en cada interna
- WebP + dimensions explícitas (anti-CLS): logos -37/-41% y og-image -78%
- particles.js self-hosted con `defer` (sin dependencia externa, no bloquea LCP)

## Pendiente (próxima sesión)
1. **og-image específica por servicio**: ahora todas las internas comparten `og-image.jpg`. Una imagen distinta por servicio mejora CTR en redes pero impacto SEO directo es bajo.
2. **Pixel de Meta**: pendiente decisión cuando se planifiquen ads en Instagram/Facebook.
3. **Limpieza de archivos antiguos en el hosting**: `firmas/`, `instagram/`, `assets/Logotipo_*.png`, `assets/851.jpg`, `assets/bg-ai.png`, `default.php`, `relay.php`, `.git` viejo. Quedaron del setup previo. Decidir cuáles quitar.
4. **Análisis de datos en Search Console + GA4** tras 1-2 semanas de recolección: ver keywords con posiciones 5-15 (oportunidades de quick wins), páginas con mejor/peor performance, fuentes de tráfico.

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
