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

# Deploy:
# Subida manual / SCP al hosting de Hostinger (ver skill "deploy")
```

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
