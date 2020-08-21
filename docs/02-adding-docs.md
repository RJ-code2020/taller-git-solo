---
id: 02-adding-docs
title: Agregando un doc a Docusaurus
---

Este es un minimanual para crear pages

## Ubicación de los pages
La carpeta `docs` guarda los pages que se deben crear con lenguaje Markdown.
```
.
├── docker-compose.yml
├── Dockerfile
├── docs
│   ├── 01-getting-started.md
│   ├── 02-adding-docs.md
│   ├── 03-challenge.md
│   └── api-docs.md
├── README.md
└── website
    ├── blog
    ├── build
    ├── core
    ├── i18n
    ├── node_modules
    ├── package.json
    ├── pages
    ├── README.md
    ├── sidebars.json
    ├── siteConfig.js
    ├── static
    └── yarn.lock
```

## Estructura de un page
Dentro de docs, se crean varios pages con diferentes nombres. Un page tiene un `id` y un `title`, luego de la sección de datos, sigue el código Markdown que se mostrará en la página web.
```yaml
---
id: id-unico
title: titulo del page
---
# codigo markdown
# codigo markdown
```

## Registro de un page
El registro de un page se realiza en archivo `sidebars.json`, ubicada en `project-name/website/sidebars.json`:
```json
{
  "docs": {
    "Taller Git": [
      "01-getting-started",
      "02-adding-docs"
    ],
    "Team": [
      "03-challenge"
    ]
  },
  "docs-other": {
    "Other Category": [
      "api-docs"
    ]
  }
}
```

Dentro del campo `docs` se registran los `ids` de los pages en el orden en que se desee mostrar. Por ejemplo, si deseamos agregar un page con id `04-nuevo-feature` dentro de la opción de Docs de la página web, quedaria de la siguiente manera:
```json
{
  "docs": {
    "Taller Git": [
      "01-getting-started",
      "02-adding-docs",
      "04-nuevo-feature"
    ],
    "Team": [
      "03-challenge"
    ]
  },
  "docs-other": {
    "Other Category": [
      "api-docs"
    ]
  }
}
```
