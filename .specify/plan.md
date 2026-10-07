# PLAN DE ARQUITECTURA TECNICA: MORATILLO WEB (AGENT-NATIVE NIVEL 5)

## 1. Stack Tecnologico
- **Framework Base:** Astro (SSG, Salida Estatica Pura `output: 'static'`).
- **Compilador y Bundler:** Compilador Rust + Vite con Rolldown (Astro 7).
- **Estilos:** Tailwind CSS v4 con variables semanticas y sistema de tokens de galeria de arte.
- **Renderizado del Boceto Inicial:** Modulo interactivo de demostracion con selector de obra, selector de variantes de prints y cotizador de envios.
- **Despliegue:** GitOps automatizado mediante script Python FTP hacia Hostinger LiteSpeed Web Server.

## 2. Resolucion del Modulo Comercial (Tienda sin sobrecarga de base de datos)
Dado que Astro es un generador de contenido estatico y no un motor de e-commerce transaccional con base de datos pesada:
- **Estructura de Ficha de Producto:**
  - Componente de seleccion de tamano con actualizacion reactiva de precio en cliente (Vanilla JS liviano, Zero-JS de frameworks pesados).
  - Selector de divisas (USD / EUR / PEN).
  - Logica de compra:
    - **Canal 1 (Automatizado):** Enlace directo a Stripe Payment Link configurado con calculo de gastos de envio segun pais.
    - **Canal 2 (Concierge VIP):** Enlace dinamico a WhatsApp con mensaje parametrizado segun la obra y dimensiones seleccionadas.
    - **Canal 3 (Originales de Alto Ticket):** Formulario modal de cotizacion y reserva privada para coleccionistas.

## 3. Capa Agendica y Semantica (GEO/AEO)
- `public/robots.txt`: Permisos expresos para bots de IA (GPTBot, ClaudeBot, PerplexityBot, etc.) y Content Signals.
- `public/llms.txt`: Manifiesto canonico para motores RAG bajo la formula Chunks E1b.
- `src/layouts/Layout.astro`: Grafo JSON-LD maestro interconectado con identificadores `@id`. Sin scripts autocerrados para cumplir las reglas estrictas del compilador Rust de Astro.

## 4. Estructura del Repositorio
```text
moratillo-web/
├── .specify/
│   ├── specify.md
│   ├── plan.md
│   └── tasks.md
├── public/
│   ├── obras/ (las 26 imagenes originales de archivo)
│   ├── llms.txt
│   ├── robots.txt
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Navbar.astro
│   │   ├── Hero.astro
│   │   ├── Manifest.astro
│   │   ├── GalleryOriginals.astro
│   │   ├── StorePrints.astro
│   │   ├── Architecture.astro
│   │   ├── ContactForm.astro
│   │   └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
├── astro.config.mjs
├── package.json
└── README.md
```
