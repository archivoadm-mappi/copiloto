# Copiloto — Tu salud, clara.

App web de copiloto de salud con IA. Analiza historias clínicas y genera alertas, consejos y chat personalizado.

## Estructura
```
copiloto/
├── index.html        ← Frontend completo
├── api/
│   └── claude.js     ← Proxy serverless (oculta la API key)
├── vercel.json       ← Configuración de Vercel
└── README.md
```

## Despliegue en Vercel (gratis, 5 minutos)

### Paso 1 — Crear cuenta en Vercel
Ve a [vercel.com](https://vercel.com) y crea una cuenta gratuita con tu email o GitHub.

### Paso 2 — Instalar Vercel CLI
```bash
npm install -g vercel
```

### Paso 3 — Desplegar
Desde la carpeta del proyecto:
```bash
vercel
```
Sigue las instrucciones (acepta todo por defecto). Al final te da una URL pública.

### Paso 4 — Agregar la API Key (MUY IMPORTANTE)
En el dashboard de Vercel:
1. Ve a tu proyecto → Settings → Environment Variables
2. Agrega: `ANTHROPIC_API_KEY` = `sk-ant-tu-key-aqui`
3. Haz redeploy: `vercel --prod`

¡Listo! La app está en internet y la API key nunca queda expuesta al usuario.

## Desarrollo local
```bash
npm install -g vercel
vercel dev
```
Crea un archivo `.env.local` con:
```
ANTHROPIC_API_KEY=sk-ant-tu-key-aqui
```

## Costos estimados
- Vercel: **gratis** (plan hobby, hasta 100GB bandwidth/mes)
- Anthropic API (Haiku): ~$0.01 USD por análisis completo
- Con 100 usuarios activos/mes: ~$1-2 USD/mes en API
