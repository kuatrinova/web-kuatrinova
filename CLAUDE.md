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

⚠️ **NO usar el "Implementar" del panel Git de Hostinger**. Crea un subdirectorio `public_html/public_html/` y rompe el deploy.

**Flujo correcto:**
```bash
# 1. Local: hacer cambios y push a GitHub
git add -A && git commit -m "..." && git push origin main

# 2. Conectar SSH a Hostinger Web Hosting:
ssh -p 65002 u846574029@77.37.52.87
# (la contraseña la cambia Carlos cada cierto tiempo, preguntar antes)

# 3. Deploy via git reset (forzar sincronización con remoto):
cd ~/domains/kuatrinova.es/public_html
export GIT_PAGER=cat
git fetch origin main
git reset --hard origin/main

# 4. Verificar:
grep -c "GTM-TMTDNCJ3" index.html  # debería ser 2
```

**Archivos NO trackeados en git que el hosting tiene en el raíz** (no tocar): `firmas/`, `instagram/`, `default.php`, `relay.php`, `assets/851.jpg`, `assets/Logotipo_*.png`, `assets/bg-ai.png`. `git reset --hard` no los borra (están en `.gitignore` o son untracked).

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
