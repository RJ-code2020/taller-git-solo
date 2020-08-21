---
id: 03-challenge
title: "Desafío del taller: mi equipo"
---

El desafío consiste en que los miembros del equipo se presenten en estos pages, uno cada uno, así como el equipo, y se pueda publicar en GitLab pages. __¡Buena suerte!__

# A cumplir
- se debe presentar uno en cada página
- una página para el equipo en general (no debe ser extenso)
- cada página debe describir al integrante (nombre y pasatiempos)

# Pasos
1. Ubica, en el proyecto de `git-saurus`, se encuentra una carpeta `docs`. Ahí deben encontrarse los pages que creen.

2. Crea la rama `develop` desde el master que compartirán todos los desarrolladores (integrantes del equipo)
```bash
git checkout master
git checkout -b develop
```

3. Distribuye el trabajo entre los demás bajo una estrategia (tener en cuenta el merge)

4. Crea tu propia rama `feat/<caracteristica-que-voy-a-agregar>` y trabaja en esa rama
```bash
git checkout develop
git checkout -b feat/doc-arturo-presentation
```

5. Fusionen sus cambios en el `develop`

6. Fusionen sus cambios ahora en el `master` y suban esta rama a GitLab
```
git push origin master
```

__Observación:__ recuerda configurar tu proyecto para que se despliegue correctamente (debes crear otra rama para cumplir con esta tarea)

# Recursos
Para escribir estos pages, se hace uso de __Markdown__. Aquí dejamos un link para conocer sobre su uso.
- [Markdown guide](https://guides.github.com/features/mastering-markdown/).

```python
print("puedo colocar código!!")
```
