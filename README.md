# Sancti Spiritus — Hospital Clinico Quirurgico

Sitio web one-pager para el **Hospital Clinico Quirurgico Sancti Spiritus** en San Cristobal Verapaz, Alta Verapaz, Guatemala.

> **Produccion:** https://www.hcqss.com  
> **Repo:** https://github.com/Darturo9/Sancti-Spiritus  
> **Dev:** `npm run dev` → `http://localhost:4321`

---

## Stack

| Capa | Tecnologia |
|------|------------|
| Framework | Astro 5.18 (SSG) |
| CSS | Tailwind CSS v3 + CSS vanilla scoped |
| JS | Vanilla JS (sin React, jQuery, Bootstrap, OwlCarousel) |
| Tipografia | Montserrat (headings) + Inter (body) via Google Fonts |
| Iconos | SVG inline (Lucide-style) |
| Deploy | Static HTML en `dist/` |

---

## Estructura del proyecto

```
sancti-spiritus/
├── public/
│   ├── _headers                  # Cache + seguridad
│   ├── site.webmanifest          # PWA manifest
│   └── favicon.ico / .png        # Favicons (6 formatos)
├── src/
│   ├── components/
│   │   ├── EmergencyBar.astro    # Barra roja emergencias 24/7
│   │   ├── Navbar.astro          # Sticky nav + drawer mobile
│   │   ├── Footer.astro          # 4-columnas con logo, horarios, contacto, copyright
│   │   ├── FloatingWhatsApp.astro # Boton flotante WhatsApp con popover de confirmacion
│   │   └── sections/
│   │       ├── Hero.astro        # Carrusel 3 slides (equipo medico, hospital, logo) + texto animado + dots responsivos
│   │       ├── About.astro       # Sobre Nosotros: texto institucional, 4 highlights, logo, 2 fotos del hospital
│   │       ├── Gallery.astro     # 4 fotos lado a lado con overlay
│   │       ├── Services.astro    # 6 servicios visibles + 6 expandibles
│   │       ├── Reviews.astro     # Carrusel testimonios infinito con clones
│   │       └── Faq.astro         # Acordeon con 5 preguntas frecuentes del docx del bot
│   ├── layouts/
│   │   └── BaseLayout.astro      # HTML base + OG tags + favicons
│   ├── pages/
│   │   ├── index.astro           # One-pager con las 6 secciones
│   │   └── 404.astro             # Pagina de error personalizada
│   └── styles/
│       └── global.css            # Directivas Tailwind + utilidades base
├── tailwind.config.mjs           # Paleta de colores del hospital (MD3)
├── astro.config.mjs              # site: hcqss.com + Tailwind integration
└── package.json                  # Astro 5 + Tailwind 3
```

---

## Secciones

| # | Seccion | Contenido |
|---|---------|-----------|
| 1 | **Hero** | Carrusel fade con 3 fotos reales (equipo medico, hospital, logo institucional) + texto animado ("Cuidamos tu salud/familia/futuro"). CTA apunta a Servicios. Sin gradiente azul en overlay. |
| 2 | **About** | Texto institucional del hospital + 4 highlights (24/7, +20 años, 12+ servicios, 5 especialidades) + logo + 2 fotos apiladas a la derecha |
| 3 | **Gallery** | 4 fotos del hospital lado a lado con overlay (Tecnologia, Atencion Humanizada, Profesionalismo, Atencion al detalle) |
| 4 | **Servicios** | Grid con 6 servicios principales, boton expandir para ver 6 mas (12 total) |
| 5 | **Reviews** | Carrusel infinito de testimonios con clones, auto-rotacion cada 5s |
| 6 | **FAQ** | Acordeon con 5 preguntas frecuentes (parqueo, citas, sin cita, laboratorio, pagos). Datos extraidos del documento del bot de WhatsApp del hospital |

---

## Caracteristicas

- **100% fotos propias** del hospital, convertidas de RAW a WebP optimizado y servidas via Cloudinary CDN
- **0 dependencias de UI** (sin React, jQuery, Bootstrap, OwlCarousel)
- **Open Graph** tags completos para previsualizacion al compartir
- **Animaciones** fade-in al scroll con IntersectionObserver
- **Boton "Volver arriba"** aparece al scrollear >600px, posicionado a la izquierda
- **Boton flotante WhatsApp** con popover de confirmacion antes de abrir el chat. Clic en cualquier parte del boton (bordes o centro/SVG) funciona correctamente.
- **Nav activo** se ilumina segun seccion visible, actualiza URL hash
- **Responsive** mobile-first con breakpoints en 640, 768, 1024px
- **Accesibilidad**: alt texts, aria-labels, focus-visible, heading order, contraste, touch targets
- **Seguridad**: headers HSTS, XFO, COOP, nosniff, referrer-policy, permissions-policy
- **Cache**: 1 año para imagenes, 1 mes para CSS/JS, 1 semana para favicons
- **`prefers-reduced-motion`** respetado en animaciones

---

## Datos del hospital

| Dato | Valor |
|------|-------|
| Nombre | Hospital Clinico Quirurgico Sancti Spiritus |
| Director | Dr. Misael Toboso Navarro |
| Direccion | 4ta. Calle 1-91, Zona 3, Barrio San Sebastian, San Cristobal Verapaz, Alta Verapaz |
| Referencia | Frente a la capilla del barrio |
| Telefono | 7950-4789 |
| WhatsApp | 4303-6016 |
| Instagram | @hospital_sancti_spiritus_gt |
| Facebook | facebook.com/profile.php?id=61590210207134 |
| Sitio web | https://www.hcqss.com |

---

## Comandos

| Comando | Accion |
|---------|--------|
| `npm install` | Instalar dependencias |
| `npm run dev` | Servidor local en `localhost:4321` |
| `npm run build` | Build a produccion en `dist/` |
| `npm run preview` | Previsualizar el build localmente |

---

## Lighthouse (ultima auditoria)

| Categoria | Score |
|-----------|-------|
| Performance | 97 |
| Accessibility | 96 |
| Best Practices | 96 |
| SEO | 100 |
