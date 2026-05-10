# CLAUDE.md — Instrucciones para agentes Claude Code

## Lectura obligatoria al iniciar sesión
1. ARCHITECTURE.md
2. CONVENTIONS.md
3. /memory/progress.md
4. DECISIONS.md

## Proyecto
- **Nombre:** Landing Page — Kuatrinova
- **Descripción:** Sitio web estático de marketing de Kuatrinova, servido en https://kuatrinova.es. Title: "Kuatrinova | Automatización e IA para Empresas". Páginas de servicios: auditoría, automatización, chatbots, dashboards, diseño, implementación, integraciones.
- **Stack:** HTML5 + CSS3 + JavaScript vanilla
- **Entorno:** Producción en Hostinger — https://kuatrinova.es

## Comandos útiles
```bash
# Desarrollo local:
# Abrir index.html directamente en el navegador, o servir con:
#   python3 -m http.server 8000

# Tests:
# No hay suite de tests automatizada (sitio estático)
```

## Flujo de deploy — kuatrinova.es

✅ **Auto-deploy configurado** vía GitHub Actions. Cada `git push origin main` dispara `.github/workflows/deploy.yml` que conecta por SSH al hosting con clave dedicada y hace `git reset --hard origin/main`. ~10-15 segundos.

**Flujo correcto:**
```bash
# Solo local: hacer cambios y push
git add -A && git commit -m "..." && git push origin main
# ya está — GitHub Actions despliega solo
```

Ver estado del deploy:
```bash
gh run list --workflow=deploy.yml --limit 3
gh run view <RUN_ID> --log
```

⚠️ **NO usar el "Implementar" del panel Git de Hostinger**. Crea un subdirectorio `public_html/public_html/` y rompe el deploy. El auto-deploy de GitHub Actions usa SSH + `git reset --hard`, NO el panel Git de Hostinger.

**Si necesitas un deploy manual de emergencia** (workflow caído, GitHub Actions deshabilitado):
```bash
ssh -p 65002 u846574029@77.37.52.87
cd ~/domains/kuatrinova.es/public_html
export GIT_PAGER=cat
git fetch origin main && git reset --hard origin/main
```

**Archivos NO trackeados en git que el hosting tiene en el raíz** (no tocar): `firmas/`, `instagram/`, `default.php`, `relay.php`, `assets/851.jpg`, `assets/Logotipo_*.png`, `assets/bg-ai.png`. `git reset --hard` no los borra (son untracked en este repo).

**Secrets de GitHub** (configurados en repo `kuatrinova/web-kuatrinova`):
- `DEPLOY_SSH_KEY` — clave privada ED25519 dedicada (la pública vive en `~/.ssh/authorized_keys` del hosting)
- `DEPLOY_HOST`, `DEPLOY_PORT`, `DEPLOY_USER`, `DEPLOY_PATH`

## Reglas de trabajo — OBLIGATORIAS

### 🔴 Nunca ejecutar sin confirmar
- Borrar archivos o directorios
- Modificar base de datos (ALTER, DROP, DELETE masivo)
- Cambiar .env o configuración de entorno
- Deploy a producción

### ✅ Flujo correcto
1. Proponer el plan antes de actuar
2. Esperar confirmación explícita del usuario
3. Ejecutar en pasos pequeños y verificables
4. Actualizar /memory/progress.md al terminar cada sesión

### Estilo de código
- Comentarios en español
- camelCase para variables y funciones
- async/await con try/catch siempre
- Seguir patrones existentes, no inventar nuevos sin consultar
