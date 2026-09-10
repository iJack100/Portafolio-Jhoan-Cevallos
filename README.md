# Jhoan Cevallos — Portafolio Personal

Carta de presentación y catálogo centralizado de mis proyectos de ingeniería de software.

**En vivo:** [jcevallos.xyz](https://jcevallos.xyz)

## Perfil Profesional

Estudiante de Ingeniería de Software en la Universidad Estatal de Milagro (UNEMI).
Mi interés principal está en la construcción del lado del servidor: arquitecturas
escalables, diseño eficiente de bases de datos y desarrollo de APIs.

## Stack Tecnológico

| Área | Herramientas |
| --- | --- |
| Backend | Python (FastAPI, Django) |
| Bases de datos | PostgreSQL, SQL Server, Oracle SQL |
| Sistemas & hardware | C++, FreeRTOS, ESP32 |
| Arquitectura | Microservicios, OOP, modelado relacional |
| Datos | Microsoft Fabric, Power BI |
| Frontend (este sitio) | HTML5, CSS3, JavaScript |

## Estructura del Repositorio

```
.
├── index.html     # Sitio completo: markup, estilos y scripts en un solo archivo
├── 404.html       # Página de error para GitHub Pages
├── og-image.png   # Vista previa 1200×630 para redes sociales
├── robots.txt     # Indexación + referencia al sitemap
├── sitemap.xml    # Sitemap de una sola URL
└── CNAME          # Dominio personalizado (jcevallos.xyz)
```

Sin dependencias, sin build, sin framework: una sola petición HTML más las
tipografías de Google Fonts. El objetivo es carga rápida y mantenimiento trivial.

## Detalles Técnicos

- **Responsive** con `clamp()` para la escala tipográfica y grids `auto-fit`;
  un único breakpoint (640px) para la navegación.
- **Accesibilidad:** enlace para saltar al contenido, `:focus-visible` en todos
  los controles, landmarks semánticos y soporte de `prefers-reduced-motion`.
- **SEO:** meta description, canonical, Open Graph, Twitter Card y datos
  estructurados JSON-LD (`schema.org/Person`).
- **Progresivo:** las animaciones de entrada sólo se activan si hay JavaScript;
  sin él, el contenido se muestra completo.
- **Impresión:** hoja de estilos `@media print` para exportar el portafolio a PDF.

## Desarrollo Local

Basta con abrir `index.html` en el navegador. Para que rutas como `/404.html`
se comporten igual que en producción, se puede levantar un servidor estático:

```bash
python -m http.server 8000
```

## Pendientes

Buscar `TODO` en `index.html` — quedan tres marcadores por completar:

- [ ] URL real del perfil de LinkedIn
- [ ] Correo de contacto (aparece en el encabezado y en la sección Contacto)
- [ ] Enlace directo al repositorio de cada proyecto (hoy apuntan al perfil de GitHub)

## Despliegue

Publicado con GitHub Pages sobre el dominio personalizado definido en `CNAME`.
Cada push a la rama principal actualiza el sitio.
