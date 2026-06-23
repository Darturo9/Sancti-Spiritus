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
│   ├── favicon.ico / .png        # Favicons (6 formatos)
│   └── images/
│       ├── logo.png / logo-nav.png
│       ├── hero-*.webp           # 3 slides + 1 mobile
│       └── gallery-*.webp        # 2 fotos
├── src/
│   ├── components/
│   │   ├── EmergencyBar.astro    # Barra roja emergencias 24/7
│   │   ├── Navbar.astro          # Sticky nav + drawer mobile
│   │   ├── Footer.astro          # 4-columnas con logo, horarios, contacto, copyright
│   │   └── sections/
│   │       ├── Hero.astro        # Carrusel 3 slides + texto animado sincronizado
│   │       ├── About.astro       # Director medico + reel Instagram
│   │       ├── Gallery.astro     # 2 fotos lado a lado con overlay
│   │       ├── Services.astro    # 6 servicios visibles + 6 expandibles
│   │       ├── Reviews.astro     # Carrusel testimonios infinito con clones
│   │       └── Booking.astro     # Formulario que envia datos por WhatsApp
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
| 1 | **Hero** | Carrusel fade con 3 fotos reales + animacion de texto sincronizada ("Cuidamos tu salud/familia/futuro") |
| 2 | **About** | Dr. Misael Toboso Navarro + reel de Instagram con `loading="lazy"` |
| 3 | **Gallery** | 2 fotos del hospital lado a lado |
| 4 | **Servicios** | Grid con 6 servicios principales, boton expandir para ver 6 mas (12 total) |
| 5 | **Reviews** | Carrusel infinito de testimonios con clones, auto-rotacion cada 5s |
| 6 | **Booking** | Formulario con validacion nativa, envia datos formateados por WhatsApp al 4303-6016 |

---

## Caracteristicas

- **100% fotos propias** del hospital, convertidas de RAW a WebP optimizado
- **0 dependencias de UI** (sin React, jQuery, Bootstrap, OwlCarousel)
- **Open Graph** tags completos para previsualizacion al compartir
- **Animaciones** fade-in al scroll con IntersectionObserver
- **Boton "Volver arriba"** aparece al scrollear >600px
- **Nav activo** se ilumina segun seccion visible, actualiza URL hash
- **Responsive** mobile-first con breakpoints en 640, 768, 1024px
- **Accesibilidad**: alt texts, aria-labels, focus-visible, heading order, contraste, touch targets
- **Seguridad**: headers HSTS, XFO, COOP, nosniff, referrer-policy, permissions-policy
- **Cache**: 1 ano para imagenes, 1 mes para CSS/JS, 1 semana para favicons
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
| Performance | 80+ |
| Accessibility | 97+ |
| Best Practices | 95+ |
| SEO | 100 |
